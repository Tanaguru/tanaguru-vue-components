<template>
  <section>
    <h2>Buttons</h2>

    <!--
      - btn btn--shadow btn--icon btn--top
      - btn btn--nude 
      - btn btn--default
      - btn btn--nude btn--icon
      - btn btn--default btn--icon
      - btn btn-pagination btn-pagination--before
      - btn btn-pagination btn-pagination--next
      - btn tabs__btn
      - btn btn--nude btn-menu is-active
      - btn btn--nude btn--logout
      - btn btn--default btn--icon 

      x btn btn--icon btn--nude btn-delete
      x btn btn--default btn-create 
      x btn btn--default btn-modify
    -->
    
    <h3>Icon + text button</h3>
    <TextButton content="Test">
      <icon-logout/>
    </TextButton>

    <h3>Text button</h3>
    <TextButton content="Test"/>

    <h3>Bordered button with icon</h3>
    <BorderedButton content="Test">
      <icon-checked/>
    </BorderedButton>

    <h3>Bordered button without icon</h3>
    <BorderedButton content="Test" />

    <h3>First pagination button</h3>
    <FirstPaginationButton/>

    <h3>Previous pagination button</h3>
    <PrevPaginationButton/>

    <h3>Next pagination button</h3>
    <NextPaginationButton/>

    <h3>Last pagination button</h3>
    <LastPaginationButton/>

    <h3>Close modal button</h3>
    <CloseModalButton/>

    <h3>Tab button</h3>
    <TabButton content="Tab 1" :isActive="isActive"/>

    <h3>Menu button</h3>
    <MenuButton openContent="Open" closedContent="Close" :burgerOpen="burgerOpen" pannelId="menu-list"/>

    <h3>Mobile log in/out button</h3>
    <MobileLogButton content="Log out" />

    <h3>Sort button</h3>
    <SortButton content="A to Z" :pressed="firstToLast" :firsToLast="firstToLast" @click="toggleOrder"/>

    <BackToTop/>

  </section>
</template>

<script>
import TextButton from '../components/Buttons/TextButton.vue';
import PrevPaginationButton from '../components/Buttons/PrevPaginationButton.vue';
import FirstPaginationButton from '../components/Buttons/FirstPaginationButton.vue';
import LastPaginationButton from '../components/Buttons/LastPaginationButton.vue';
import NextPaginationButton from '../components/Buttons/NextPaginationButton.vue';
import BorderedButton from '../components/Buttons/BorderedButton.vue';
import BackToTop from '../components/Buttons/BackToTop.vue';
import CloseModalButton from '../components/Buttons/CloseModalButton.vue';
import TabButton from '../components/Buttons/TabButton.vue';
import MenuButton from '../components/Buttons/MenuButton';
import MobileLogButton from '../components/Buttons/MobileLogButton';
import SortButton from '../components/Buttons/SortButton';

import IconChecked from '../components/icons/IconChecked';
import IconLogout from '../components/icons/IconLogout';

export default {
  name: 'DemoButtons',
  components: {
    TextButton,
    PrevPaginationButton,
    FirstPaginationButton,
    LastPaginationButton,
    NextPaginationButton,
    CloseModalButton,
    BackToTop,
    BorderedButton,
    TabButton,
    MenuButton,
    MobileLogButton,
    SortButton,

    IconChecked,
    IconLogout
  },
  data(){
    return {
      burgerOpen: false,
      isActive: true,
      pressed: true,
      firstToLast: true,
    }
  },
  methods: {
    toggleOrder(){
      this.firstToLast = !this.firstToLast
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
  section {
    margin-left: 5%;
  }
</style>