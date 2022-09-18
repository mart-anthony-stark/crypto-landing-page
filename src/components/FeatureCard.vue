<template>
  <div class="card">
    <img class="icon" src="../assets/svg/features/manage.svg" alt="feature" />
    <div class="content">
      <h3>Manage Portfolio</h3>
      <p>
        Buy and sell popular digital currencies, keep track of them in the one
        place.
      </p>
    </div>
    <a class="see"
      >See Explained <img src="../assets/svg/features/arrow.svg" alt="see more"
    /></a>
  </div>
</template>

<style scoped>
@import "../css/variables.css";

.card {
  width: 296px;
  height: 343px;

  /* High Fidelity Color/Card Background */

  background: rgba(255, 255, 255, 0.02);
  border: 1px solid rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(200px);
  /* Note: backdrop-filter has minimal browser support */

  border-radius: 18px;

  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-between;
  padding: 2rem;
}

.icon {
  height: 80px;
}

.content h3 {
  margin-bottom: 1rem;
}

.see {
  display: flex;
  align-items: center;
  gap: 15px;
  color: var(--c-accent);
  cursor: pointer;
}
</style>