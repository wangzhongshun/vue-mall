<template>
  <div class="message-content w10">
    <ul class="msg">
      <li>
        <img src="../../assets/images/lit.png" height="50" width="50"/>
        <i class="icon-msg"></i>
        <p>物流</p>
      </li>
      <li>
        <img src="../../assets/images/infor.png" height="50" width="50"/>
        <i class="icon-msg"></i>
        <p>通知</p>
      </li>
    </ul>
    <div class="lit-line"></div>
    <ul class="msg-c">
      <li v-for="(item,index) of datalist">
        <p class="clearfix">
          <span class="fl" v-if="sendStatus == '00'">发货状态:未发货</span>
          <span class="fl" v-if="sendStatus == '01'">发货状态:已发货</span>
          <span class="fl" v-if="sendStatus == '02'">发货状态：部分发货</span>
          <time class="fr">今天12:10</time>
        </p>
        <p>
          你所购买的{{item.productName}}，。
        </p>
        <p>
          订单编号:{{item.ordersOrderNo}}
        </p>
      </li>
<!--      <li>
        <p class="clearfix">
          <span class="fl">商品已发货</span>
          <time class="fr">今天12:10</time>
        </p>
        <p>
          你所购买的海底捞速食火锅，已经发货。
        </p>
        <p>
          订单编号:47841641461
        </p>
      </li>-->
    </ul>
  </div>
</template>

<script>
    export default {
        name: "message-content",
        props:["datalist"],
    }
</script>

<style scoped>
  @import '../../assets/css/message/message-c.css';
</style>
