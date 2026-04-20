<template>
  <footer class="mobile-footer">
    <a href="https://github.com/femigabriel" target="_blank" rel="noreferrer">
      <i class="lab la-github"></i>
      GitHub
    </a>
    <a
      href="https://www.linkedin.com/in/gabriel-oluwafemi"
      target="_blank"
      rel="noreferrer"
    >
      <i class="lab la-linkedin"></i>
      LinkedIn
    </a>
    <a href="https://twitter.com/FemiGab2018" target="_blank" rel="noreferrer">
      <i class="lab la-twitter"></i>
      Twitter
    </a>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
.mobile-footer {
  border: 1px solid rgba(148, 163, 184, 0.2);
  border-radius: 14px;
  padding: 12px;
  display: flex;
  justify-content: space-between;
  gap: 8px;
  background: rgba(15, 23, 42, 0.6);
}

.mobile-footer a {
  display: inline-flex;
  align-items: center;
  gap: 5px;
  text-decoration: none;
  color: #cbd5e1;
  font-size: 0.85rem;
}

.mobile-footer a:hover {
  color: #22d3ee;
}

@media (min-width: 641px) {
  .mobile-footer {
    display: none;
  }
}
</style>
