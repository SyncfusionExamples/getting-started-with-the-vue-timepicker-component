<template>
  <div class="wrapper">
    <ejs-timepicker placeholder="Select a time"
      :value="timeValue"
      :min="minTime"
      :max="maxTime"
      :enableMask="true"
      format="HH:mm"
      step="60"></ejs-timepicker>
  </div>
</template>

<script>
import {TimePickerComponent, MaskedDateTime} from '@syncfusion/ej2-vue-calendars';

export default {
  name: 'App',
  components: {
    "ejs-timepicker": TimePickerComponent
  },
  data(){
    return{
      timeValue: new Date("09/12/2022 12:00 PM"),
      minTime: new Date("09/12/2022 09:00 AM"),
      maxTime: new Date("09/12/2022 05:00 PM"),
    }
  },
  provide:{
    timepicker: [MaskedDateTime]
  }
}
</script>

<style>
  @import '../node_modules/@syncfusion/ej2-base/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-inputs/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-popups/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-lists/styles/material.css';
  @import "../node_modules/@syncfusion/ej2-vue-calendars/styles/material.css";

  .wrapper{
    max-width: 250px;
    margin: 0 auto;
  }
</style>
