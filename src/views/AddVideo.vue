<template>
    <a-form
    :model="formState"
    name="inputSearch"
    autocomplete="off"
    @onSearch="onSearch"
  >

      
      
      <a-input-search
        v-model:value="formState.inputSearch"
        placeholder="input search text"
        enter-button="Search"
        size="large"
        @search="onSearch"
      />
      <a-input-search
        v-model:value="value"
        placeholder="input search text"
        size="large"
        @search="onSearch"
      />
       
    </a-form>
  </template>
  <script lang="ts">
    import { defineComponent, ref, reactive } from 'vue';
    import { Form } from "ant-design-vue";
    import "ant-design-vue/dist/antd.css";
    interface FormState {
  inputSearch: string;
}
  export default defineComponent({
    setup() {
        const value = ref<string>('');
        const formState = reactive<FormState>({
      inputSearch: 'hola'
    });
  
      const onSearch = (searchValue: string) => {
        console.log('use value', searchValue);
        console.log('or use this.value', formState.inputSearch);
      };
  
      return {
        value,
        formState,
        onSearch,
      };
    },
  });
  </script>
  