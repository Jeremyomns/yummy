<template>
  <div id="app">
    <header>
      <h1 class="app-title">Yummy</h1>
    </header>
    <main>
      <section>
        <h2 class="section-title">Planning</h2>
        <table class="week-table">
          <thead>
            <tr>
              <th></th>
              <th>Petit-déjeuner</th>
              <th>Déjeuner</th>
              <th>Dîner</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="day in weekDays" :key="day">
              <td>{{ day }}</td>
              <td contenteditable="true">{{ planning[day].breakfast }}</td>
              <td contenteditable="true">{{ planning[day].lunch }}</td>
              <td contenteditable="true">{{ planning[day].dinner }}</td>
            </tr>
          </tbody>
        </table>
      </section>
      <section>
        <h2 class="section-title">Repas avec viande</h2>
        <div> 
          <div>1</div>
            <div>2</div>
            <div>3</div>
            <div>4</div>
        </div>
        <h3 class="section-title">Repas sans viande</h3>
            <div>1</div>
            <div>2</div>
            <div>3</div>
            <div>4</div>
      </section>
    </main>
    <footer>
      <!-- Votre pied de page ira ici -->
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      weekDays: ['Lundi', 'Mardi', 'Mercredi', 'Jeudi', 'Vendredi', 'Samedi'],
      planning: {
        Lundi: { breakfast: '', lunch: '', dinner: '' },
        Mardi: { breakfast: '', lunch: '', dinner: '' },
        Mercredi: { breakfast: '', lunch: '', dinner: '' },
        Jeudi: { breakfast: '', lunch: '', dinner: '' },
        Vendredi: { breakfast: '', lunch: '', dinner: '' },
        Samedi: { breakfast: '', lunch: '', dinner: '' },
      },
    };
  },
};
</script>

<style>
body {
  margin: 0;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  background-color: #ffffff;
  /* Fond de page blanc */
}

.section-title {
  font-size: 1.5em;
  margin-top: 20px;
  color: #000;
}

.week-table {
  width: 70%;
  /* Ajustez la largeur selon vos besoins */
  margin: 0 auto;
  /* Centre le tableau horizontalement */
  border-collapse: collapse;
  margin-top: 10px;
  color: #000;
}

th,
td {
  border: 1px solid #000;
  /* Bordure noire */
  padding: 10px;
  text-align: left;
  line-height: 1.5;
  /* Ajustez la hauteur de ligne selon vos besoins */
}

th {
  background-color: #006BA6;
  color: #ffffff;
  /* Couleur du texte en noir */
}

td {
  background-color: #f9f9f9;
}

header {
  background-image: url('./assets/bolrepas.jpeg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 50% 50%;
  background-color: #f5f5f5;
  height: 100%;
  padding: 50px;
}

.app-title {
  font-size: 2em;

}
</style>
