<template>
<div id="app" class="layout ant-layout">
  <AppHeader :lang="$lang" @change-lang="setLang"/>
  <div class="content">
    <FormIntro />
    <BugReport />
  </div>
  <footer class="ant-layout-footer">
    <div class="ant-layout-footer" style="text-align: center;">
      Inspired by <a href="https://ant-design-vue.gitee.io/issue-helper" target="_blank">Ant Design Vue Issue Helper</a>
      · <a href="https://github.com/hd-ui/issue-helper">Source Code</a>
    </div>
  </footer>
</div>
</template>

<script lang="babel">
import { getQuery, updateQuery } from '../helpers'

import FormIntro from './FormIntro.vue'
import AppHeader from './AppHeader.vue'
import BugReport from './BugReport.vue'

export default {
  name: 'App',

  components: {
    FormIntro,
    AppHeader,
    BugReport,
  },
  methods: {
    setLang (lang) {
      this.$lang = lang
      updateQuery({ lang })
    },
  },
}
</script>




