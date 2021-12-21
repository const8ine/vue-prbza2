<template>
  <div id="app">
    <Akt1
      msg="adasdas"
      :doc="{
        city: 'Москва',
        companyName: 'Название',
        year: 2022,
        day: '01',
        monthFull: 'января',
        contract: {
          number: 15,
          day: '01',
          month: '12',
          monthFull: 'декабря',
          year: 2021,
          subject: 'разработке программного продукта',
        },
        period: {
          start: '01 декабря',
          end: '31 декабря',
          cost: '300 000 (триста тысяч)',
        },
        contractor: 'И.И. Иванов',
        contractorFull: 'Иванов Иван Иванович',
        companyRepresentative: 'П.П. Петров',
        companyRepresentativeFull: 'Петра Петровича Петрова',
      }"
    />
  </div>
</template>

<script>
import Akt1 from './components/Akt1.vue';

export default {
  name: 'App',
  components: {
    Akt1,
  },
};
</script>

<style>
body,
body * {
  box-sizing: border-box;
}

body {
  width: 210mm;
  height: 297mm;
  padding: 20mm 10mm 20mm 20mm;
  font-family: serif;
  font-size: 12pt;
  text-align: justify;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #000;
}

h1 {
  font-size: 12pt;
  font-weight: bold;
  text-align: center;
}

.row {
  display: flex;
  flex-flow: row nowrap;
}

.row > * {
  flex: 1 1 50%;
}

.__align-right {
  text-align: right;
}

.__ml-sm {
  margin-left: 2em;
}

.__ml-md {
  margin-left: 4em;
}

.__ml-lg {
  margin-left: 6em;
}

@media screen {
  body {
    border: 1px solid #ccc;
  }
}
</style>
