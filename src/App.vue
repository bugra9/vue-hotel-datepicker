<template>
  <div id="app" style="text-align: left; padding: 10vw">
    <div>
      <div class="box">
        <DatePicker
            ref="dp"
            format="DD/MM/YYYY"
            :startingDateValue="new Date(startTime.split('.')[2], startTime.split('.')[1]-1, startTime.split('.')[0])"
            :endingDateValue="new Date(finishTime.split('.')[2], finishTime.split('.')[1]-1, finishTime.split('.')[0])"
            :startDate="new Date(new Date().getFullYear()-1, new Date().getMonth(), new Date().getDay())"
            :endDate="new Date()"
            :i18n="tr"
          ></DatePicker>
      </div>
    </div>
  </div>
</template>

<script>
import DatePicker from 'components/DatePicker.vue';

export default {
  components: {
    DatePicker
  },
  data() {
    return {
      startTime: '12.09.2017',
      finishTime: '15.10.2017',
      tr: {
        night: 'Gün',
        nights: 'Gün',
        'day-names': ['Pzt', 'Sal', 'Çar', 'Per', 'Cum', 'Cmt', 'Paz'],
        'check-in': 'Başlangıç',
        'check-out': 'Bitiş',
        'month-names': ['Ocak', 'Şubat', 'Mart', 'Nisan', 'Mayıs', 'Haziran', 'Temmuz', 'Ağustos', 'Eylül', 'Ekim', 'Kasım', 'Aralık'],
      },
    };
  }
};

</script>

<style>
body,
html {
  font-family: 'Source Sans Pro', sans-serif;
}

.box {
  width: 100%;
}
</style>
