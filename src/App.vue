<template>
    <section>
      <img :src="picture" v-bind:width="size" v-bind:height="size" ref="imageURL"/><br/>

      <!-- <form @submit.prevent="submitForm">
        <label>nickname:</label>
        <input type="text" ref="nicknameEL"/>
        <button type="submit">submit</button>
      </form> -->
      <h1>Name-LastName : {{getFullName()}}</h1>
      <!-- <h2>nickname: {{nickname}}</h2> -->
      <h1>Dob: {{dob}}</h1>
      <h1>age: {{age}}</h1>
      <p>Address : <span v-html="address"></span></p>
      <p>Social : <a :href="social" target="_blank">facebook</a></p>
      <p v-if="hobby.length === 0">no hobby</p>
      <div v-else>
        <p>hobby:</p>
        <ul>
            <li v-for="(item,index) in hobby" :key="index">{{item}}</li>
        </ul>
      </div>
      <p>ຂໍ້ມູນພື້ນຖານ:</p>
      <ul>
        <li>ເພດ: {{general.gender}}</li>
        <li>ນ້ຳໜັກ: {{general.weight}}</li>
        <li>ສ່ວນສູງ: {{general.height}}</li>
        <li>ພະຍາດປະຈຳຕົວ: {{general.status}}</li>
      </ul>
      <!-- <button @click="showData">ຄລິດເພື່ອເບິ່ງຂໍ້ມູນ</button>
      <button @click.ctrl="increment(10)">ເພີ່ມ</button>
      <button @click="decrement(5)">ຫຼຸດ</button> -->
    </section>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      firstName:"Noy",
      lastName:"Nexsiz",
      dob:"28/04/2001",
      // nickname:"",
      age:21,
      address:"<strong>Vangvieng</strong>",
      picture:"https://cdn-icons.flaticon.com/png/512/560/premium/560277.png?token=exp=1645600452~hmac=657d77c33da7866efa8da32d8e4818c7",
      size:150,
      social:"https://www.facebook.com/Noyskz/",
      hobby:["playing games", "listening to music", "playing basketball", "reading a book", "surfing internet"],
      general:{gender:"male", weight:53, height:175, status:false}
    }
  },
  methods:{
    getFullName(){
      return `${this.firstName} ${this.lastName}`
    },
    // showData(){
    //   alert(this.firstName)
    // },
    // increment(value){
    //   this.age+=value
    // },
    // decrement(value){
    //   this.age-=value
    // },
    // submitForm(){
    //   this.nickname=this.$refs.nicknameEL.value;
    // }
  }
}
</script>

<style></style>
