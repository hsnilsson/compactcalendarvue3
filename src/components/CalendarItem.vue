<template>
  <ul class="mondayfirst">
    <WeekHeader :week="weeks[0]" />
    <WeekItem
      v-for="week in weeks"
      :key="week.id"
      :week="week"
      :vacations="vacations"
      :holidays="holidays"
    />
  </ul>
</template>
<script>
import WeekItem from "./week/WeekItem.vue";
import WeekHeader from "./week/WeekHeader.vue";
export default {
  components: { WeekItem, WeekHeader },
  props: {
    mondayfirst: Boolean,
    weeks: {
      type: Array,
      default: function () {
        return [];
      },
    },
    vacations: {
      type: Object,
      default: function () {
        return {};
      },
    },
    holidays: {
      type: Array,
      default: function () {
        return [];
      },
    },
  },
};
</script>

<style scoped></style>
