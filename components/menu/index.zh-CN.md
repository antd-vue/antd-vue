<script>
export default {
  data() {
    return {
      defaultOpen: ['sub1']
    }
  },
  methods: {
    handleClick() {
      console.log('click ', e);
    }
  }
}
</script>

::: demo 顶部导航
```html
<v-menu
  :default-open-index="defaultOpen"
  mode="inline"
>
  <v-menu-item index="mail">
    <Icon type="mail"></Icon>Navigation One
  </v-menu-item>
  <v-menu-item index="app" disabled>
    <Icon type="appstore"></Icon>Navigation Two
  </v-menu-item>
  <sub-menu index="sub1">
    <template slot="title">
      <Icon type="setting"></Icon> Navigation Three - Submenu
    </template>
    <menu-item-group>
      <template slot="title">Item 1</template>
      <v-menu-item index="setting:1">Option 1</v-menu-item>
      <v-menu-item index="setting:2">Option 2</v-menu-item>
    </menu-item-group>
    <menu-item-group>
      <template slot="title">Item 2</template>
      <v-menu-item index="setting:3">Option 3</v-menu-item>
      <v-menu-item index="setting:4">Option 4</v-menu-item>
    </menu-item-group>
    <sub-menu index="sub2">
      <template slot="title">
        <Icon type="setting"></Icon> Navigation Three - Five Submenu
      </template>
      <v-menu-item index="sub2.1">Option 2.1</v-menu-item>
      <v-menu-item index="sub2.2">Option 2.2</v-menu-item>
      <v-menu-item index="sub2.3">Option 2.3</v-menu-item>
      <v-menu-item index="sub2.4">Option 2.4</v-menu-item>
    </sub-menu>
  </sub-menu>
  <v-menu-item index="alipay">
    <a href="https://ant.design" target="_blank" rel="noopener noreferrer">Navigation Four - Link</a>
  </v-menu-item>
</menu>
```
:::
