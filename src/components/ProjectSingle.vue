<template>
  <article class="project-box">
    <div class="meta-row">
      <p class="framework">{{ framework }}</p>
      <span class="pill">{{ highlight || status }}</span>
    </div>

    <h3>{{ title }}</h3>
    <p class="description">{{ description }}</p>

    <div class="bottom-row">
      <small>{{ date }}</small>
      <a target="_blank" rel="noreferrer" :href="url">
        {{ video }}
        <i class="las la-arrow-right"></i>
      </a>
    </div>
  </article>
</template>

<script>
export default {
  props: [
    "framework",
    "title",
    "status",
    "video",
    "date",
    "description",
    "url",
    "highlight",
  ],
};
</script>

<style scoped>
.project-box {
  background: linear-gradient(160deg, rgba(15, 23, 42, 0.9), rgba(15, 23, 42, 0.6));
  border: 1px solid rgba(148, 163, 184, 0.22);
  border-radius: 16px;
  padding: 18px;
  display: grid;
  gap: 14px;
  min-height: 220px;
  transition: transform 0.22s ease, border-color 0.22s ease;
}

.project-box:hover {
  transform: translateY(-3px);
  border-color: rgba(34, 211, 238, 0.55);
}

.meta-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
}

.framework {
  color: #93c5fd;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  font-size: 0.72rem;
}

.pill {
  border-radius: 999px;
  padding: 4px 10px;
  background: rgba(34, 211, 238, 0.12);
  border: 1px solid rgba(34, 211, 238, 0.35);
  color: #22d3ee;
  font-size: 0.72rem;
}

h3 {
  font-size: 1.28rem;
  line-height: 1.3;
}

.description {
  color: #94a3b8;
  line-height: 1.65;
}

.bottom-row {
  margin-top: auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
}

small {
  color: #64748b;
  font-size: 0.78rem;
}

a {
  color: #22d3ee;
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  gap: 5px;
}

a:hover {
  color: #67e8f9;
}
</style>
