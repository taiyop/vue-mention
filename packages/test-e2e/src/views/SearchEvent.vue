<script>
export default {
  data () {
    return {
      text: '',
      items: [
        {
          value: 'akryum',
          firstName: 'Guillaume',
        },
        {
          value: 'posva',
          firstName: 'Eduardo',
        },
        {
          value: 'atinux',
          firstName: 'Sébastien',
        },
      ],
      searchText: null,
    }
  },
}
</script>

<template>
  <div
    class="demo"
  >
    <Mentionable
      :keys="['@']"
      :items="items"
      @search="searchText = $event"
    >
      <textarea
        v-model="text"
        rows="6"
        class="input"
      />
    </Mentionable>

    <div class="search">{{ searchText }}</div>
  </div>
</template>
