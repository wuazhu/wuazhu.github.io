<template>
  <div class="cust-group">
    <iframe frameborder=0 width="100%" height="100%" :src="custGroupSrc"></iframe>
  </div>
</template>

<script>
export default {
  data() {
    return {
      custGroupSrc: 'http://crm.chinapost.com:8441/#label/label_market'
    }
  },
  watch: {
    $route(to) {
      switch (to.path) {
      case '/loc/prefecture/prefecture_mgr':
        this.custGroupSrc = 'http://crm.chinapost.com:8441/#prefecture/prefecture_mgr'
        break
      case '/loc/prefecture/allUserMsg_mgr':
        this.custGroupSrc = 'http://crm.chinapost.com:8441/#prefecture/allUserMsg_mgr'
        break
      case '/loc/label/category_mgr':
        this.custGroupSrc = 'http://crm.chinapost.com:8441/#label/category_mgr'
        break
      case '/loc/custom/pushSys_mgr':
        this.custGroupSrc = 'http://crm.chinapost.com:8441/#custom/pushSys_mgr'
        break
      case '/loc/custom/pushLogtrack_mgr':
        this.custGroupSrc = 'http://crm.chinapost.com:8441/#custom/pushLogtrack_mgr'
        break
      case '/loc/label/dataSource_mgr':
        this.custGroupSrc = 'http://crm.chinapost.com:8441/#label/dataSource_mgr'
        break
      case '/loc/label/label_mgr':
        this.custGroupSrc = 'http://crm.chinapost.com:8441/#label/label_mgr'
        break
      case '/loc/dimtable/dimtable_mgr':
        this.custGroupSrc = 'http://crm.chinapost.com:8441/#dimtable/dimtable_mgr'
        break
      case '/loc/label/label_market':
        this.custGroupSrc = 'http://crm.chinapost.com:8441/#label/label_market'
        break
      case '/loc/label/custom_market':
        this.custGroupSrc = 'http://crm.chinapost.com:8441/#custom/custom_market'
        break
      default:
        this.custGroupSrc = 'http://crm.chinapost.com:8441/#label/label_market'
      }
    }
  }
}
</script>
<style lang="less">
.cust-group{
  height: 98%;
}
</style>
