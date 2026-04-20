<template>
  <div class="project-single" @click="openProject">
    <div class="project-header">
      <div class="project-badge">
        <span class="highlight-badge" v-if="highlight">{{ highlight }}</span>
        <span class="status-badge" :class="statusClass">{{ status }}</span>
      </div>
      <div class="project-date">{{ date }}</div>
    </div>
    
    <h3 class="project-title">{{ title }}</h3>
    <p class="project-framework">{{ framework }}</p>
    <p class="project-description">{{ description }}</p>
    
    <div class="demo-note" v-if="demoNote">
      <i class="las la-info-circle"></i>
      <span>{{ demoNote }}</span>
    </div>
    
    <div class="project-footer">
      <span class="cta-link">{{ cta || 'Explore project' }} <i class="las la-arrow-right"></i></span>
    </div>
    
    <div class="card-glow"></div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    framework: String,
    status: String,
    date: String,
    description: String,
    highlight: String,
    url: String,
    cta: String,
    demoNote: String
  },
  computed: {
    statusClass() {
      return {
        'status-live': this.status === 'Live',
        'status-demo': this.status === 'Demo Available',
        'status-unknown': this.status === 'Status Unknown',
        'status-signup': this.status === 'Requires Signup'
      };
    }
  },
  methods: {
    openProject() {
      if (this.url) {
        window.open(this.url, '_blank');
      }
    }
  }
};
</script>

<style scoped>
.project-single {
  background: rgba(18, 22, 35, 0.6);
  border: 1px solid var(--border-light);
  border-radius: 24px;
  padding: 24px;
  cursor: pointer;
  transition: all var(--transition-smooth);
  position: relative;
  overflow: hidden;
  height: 100%;
  display: flex;
  flex-direction: column;
}

.project-single:hover {
  transform: translateY(-6px);
  border-color: rgba(34, 211, 238, 0.4);
  background: rgba(30, 35, 50, 0.7);
  box-shadow: 0 20px 30px -12px rgba(0, 0, 0, 0.3);
}

.card-glow {
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at 70% 20%, rgba(34, 211, 238, 0.08), transparent 70%);
  opacity: 0;
  transition: opacity var(--transition-smooth);
  pointer-events: none;
}

.project-single:hover .card-glow {
  opacity: 1;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 16px;
}

.project-badge {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
}

.highlight-badge {
  background: linear-gradient(135deg, rgba(34, 211, 238, 0.2), rgba(56, 189, 248, 0.1));
  color: var(--accent-cyan);
  font-size: 0.7rem;
  font-weight: 600;
  padding: 4px 10px;
  border-radius: 30px;
  border: 1px solid rgba(34, 211, 238, 0.3);
}

.status-badge {
  font-size: 0.7rem;
  font-weight: 600;
  padding: 4px 10px;
  border-radius: 30px;
  background: rgba(16, 185, 129, 0.15);
  color: #34d399;
  border: 1px solid rgba(16, 185, 129, 0.3);
}

.status-demo {
  background: rgba(34, 211, 238, 0.15);
  color: #22d3ee;
  border-color: rgba(34, 211, 238, 0.3);
}

.status-unknown {
  background: rgba(245, 158, 11, 0.15);
  color: #fbbf24;
  border-color: rgba(245, 158, 11, 0.3);
}

.status-signup {
  background: rgba(139, 92, 246, 0.15);
  color: #a78bfa;
  border-color: rgba(139, 92, 246, 0.3);
}

.project-date {
  font-size: 0.7rem;
  color: var(--text-secondary);
  font-weight: 500;
}

.project-title {
  font-size: 1.3rem;
  font-weight: 600;
  margin-bottom: 6px;
  letter-spacing: -0.02em;
}

.project-framework {
  font-size: 0.75rem;
  color: var(--accent-blue);
  margin-bottom: 14px;
  font-weight: 500;
}

.project-description {
  font-size: 0.85rem;
  color: var(--text-secondary);
  line-height: 1.5;
  margin-bottom: 16px;
  flex-grow: 1;
}

.demo-note {
  background: rgba(0, 0, 0, 0.3);
  border-radius: 12px;
  padding: 10px 12px;
  margin-bottom: 16px;
  font-size: 0.75rem;
  color: #cbd5e1;
  display: flex;
  align-items: center;
  gap: 8px;
  border-left: 2px solid var(--accent-cyan);
}

.demo-note i {
  color: var(--accent-cyan);
  font-size: 1rem;
}

.project-footer {
  margin-top: auto;
  padding-top: 16px;
}

.cta-link {
  font-size: 0.8rem;
  font-weight: 500;
  color: var(--text-primary);
  display: inline-flex;
  align-items: center;
  gap: 8px;
  transition: gap var(--transition-fast);
}

.project-single:hover .cta-link {
  gap: 12px;
  color: var(--accent-cyan);
}

.cta-link i {
  font-size: 1rem;
}
</style>