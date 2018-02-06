
 

require.ensure(['./top'], function(require){
    let top1 = require('./top1')
    that.comp1 = top1
})
v-if: 通过 v-if 加载;
components: {
      "el-button":Button,
      "agentAd":resolve => {require(['@/components/admin/agent/agent'], resolve)},
      "AgentStat":resolve => {require(['@/components/admin/agent/agentStat/agentStat'], resolve)},
      "AgentFormList":resolve => {require(['@/components/admin/agent/agentFormList/agentFormList'], resolve)}
}