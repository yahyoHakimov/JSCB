<script>

export default {
  data: () => ({
    selectedFile: null,
    imageUrl: null

  }),
  props: {
    user: {
      type: Object,
      required: true
    }
  },
  methods: {
    handleFileChanges(event) {
      this.selectedFile = event.target.files[0];
      console.log(event)
    },
  },
}
</script>

<template>

  <div class="cheque">
    <div>
      <input type="file" @change="handleFileChanges">
      <button @click="uploadImg">Rasmni yuklang</button>
      <div v-if="imageUrl">
        <img :src="imageUrl" alt="Yuklangan rasm">
      </div>
    </div>
    <!--    <img src="bank-logo.png" alt="Bank logo" class="bank-logo">-->
    <div class="bank-name">Universalbank</div>
    <div class="cheque-number">№021</div>
    <div class="payee-name">Toshmatov Muzaffar Raxmonnazarovich</div>
    <div class="amount">1 3 9 7 1</div>
    <div class="date">Amal qilish muddati: «31» dekabr 2023 yilgacha</div>
    <div class="signature">Boshqaruv Raisi <br> A.A. Buvanazarov</div>
  </div>

  <!--  <div class="num1">-->
  <!--    <div class="header" v-for="users in user">-->
  <!--&lt;!&ndash;      <img src="./logo/bank-logo.png" alt="Bank logo"> <br>&ndash;&gt;-->
  <!--      <span class="bank-name">Universalbank</span><br>-->
  <!--      <span class="name">SH.T.№</span><br>-->
  <!--      <span class="cheque-name" >Here is 5 digit:{{users.name}}</span> <br>&lt;!&ndash; 5 xonali son -&ndash;&gt;-->

  <!--      <span>Amal qilish muddati:   </span>      <span> 31 - dekabr 2023-yilgacha </span>-->
  <!--    </div>-->
  <!--    <br>-->
  <!--    <div class="payee">-->
  <!--      <span class="identity">Guvohnoma</span> <br>-->
  <!--      <span class="digit">№: {{user.username}}</span><br>-->
  <!--      <span class="fullName">Toshmatov Muzaffar Rahmonnazarovich{{}}</span> <br>-->
  <!--      <span class="department">Buvayda tumani bank boshqaruvchisi{{}}</span>-->

  <!--      <p>Boshqaruv raisi: </p> <p>A.A.Buvanazarov </p>-->

  <!--    </div>-->
  <!--  </div>-->
</template>


<style>
.cheque {
  width: 800px;
  height: 300px;
  border: 1px solid #000;
  padding: 20px;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
}

.bank-logo {
  float: left;
  width: 150px;
  height: 150px;
}

.bank-name {
  font-size: 24px;
  font-weight: bold;
  margin-top: 20px;
  color: red;
}

.cheque-number {
  font-size: 16px;
  float: right;
  margin-top: 10px;
}

.payee-name {
  font-size: 18px;
  margin-top: 50px;
}

.amount {
  font-size: 24px;
  font-weight: bold;
  margin-top: 20px;
}

.date {
  font-size: 14px;
  margin-top: 20px;
}

.signature {
  text-align: right;
  margin-top: 2px;
}
</style>