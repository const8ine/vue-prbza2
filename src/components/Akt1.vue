<template>
  <h1>
    {{ doc.msg }}
    АКТ ОКАЗАННЫХ УСЛУГ <br />
    ПО ДОГОВОРУ АВТОРСКОГО ЗАКАЗА № {{ doc.contract.number }} от
    {{ doc.contract.day }} {{ doc.contract.monthFull }}
    {{ doc.contract.year }} г.
  </h1>

  <div class="row">
    <p>г. {{ doc.city }}</p>

    <p class="__align-right">
      {{ doc.monthFull }}
      {{ doc.year }} г.
    </p>
  </div>

  <p class="__break-line">
    Общество с ограниченной ответственностью «{{ doc.companyName }}», именуемое
    в дальнейшем «Заказчик», в лице генерального директора
    {{ doc.companyRepresentativeFull }}, действующего на основании Устава, с
    одной стороны,
  </p>

  <p>
    и гр. РФ
    {{ doc.contractorFull }}, именуемый в дальнейшем «Исполнитель» с другой
    стороны, совместно именуемые Стороны, действуя добровольно, находясь в
    здравом уме и ясной памяти, подписали настоящий Акт оказанных услуг (далее —
    Акт) к Договору авторского заказа № {{ doc.contract.number }} от
    {{ doc.contract.day }}.{{ doc.contract.month }}.{{ doc.contract.year }} г.
    (далее — Договор) о нижеследующем:
  </p>

  <ol>
    <li>
      Исполнителем по заданию Заказчика и в соответствии с Договором оказаны
      услуги по {{ doc.contract.subject }} за период с {{ doc.period.start }} по
      {{ doc.period.end }} в количестве {{ doc.period.hours }} часов.
    </li>
    <li>
      Услуги по {{ doc.contract.subject }} за указанный период оказаны
      Исполнителем полностью, своевременно и надлежащим образом.
      <br />
      Претензий со стороны Заказчика к Исполнителю не имеется.
    </li>
    <li>
      В соответствии с условиями Договора Исполнитель передает, а Заказчик
      принимает/или не принимает исключительное право на результаты работ по
      договору.
    </li>
    <li>
      Стоимость оказанных услуг за указанный в п 1. настоящего акта период
      составила {{ doc.period.cost }} рублей.
    </li>
  </ol>

  <div class="row">
    <p>Заказчик</p>

    <p class="__ml-lg">Исполнитель</p>
  </div>

  <div class="row">
    <p>
      Генеральный директор
      <br />
      OOO «{{ doc.companyName }}»
    </p>

    <p class="__align-right"></p>
  </div>

  <div class="row">
    <p>___________________ {{ doc.companyRepresentative }}</p>

    <p class="__ml-lg">
      ____________________
      {{ doc.contractor }}
    </p>
  </div>
</template>

<script>
export default {
  name: 'Akt1',
  props: {
    msg: String,
    doc: {
      city: String,
      companyName: String,
      year: {
        type: Number,
        default: new Date().getFullYear(),
      },
      day: String,
      monthFull: String,
      contract: {
        number: Number,
        day: String,
        month: String,
        monthFull: String,
        year: Number,
        subject: String,
      },
      period: {
        start: String,
        end: String,
        cost: String,
      },
      contractor: String,
      contractorFull: String,
      companyRepresentative: String,
      companyRepresentativeFull: String,
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
