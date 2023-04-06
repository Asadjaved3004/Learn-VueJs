<template>
  <div>
    <!-------------input fields started----------------->
<input type="text" name="email" placeholder="Enter Email" v-model="email"/>
<br />
<br />
<input type="password" name="password" placeholder="enter Password" v-model="password"/>


    <!-------------input fields Ended----------------->
<br />
<br />
<!----------Button with clickable function named as getData()----------->

<button v-on:click="getData()">Get Details</button>

<!----------------------------Checkboxes started------------>
<h3>Technology</h3>
<label for="java">Java</label>
<input type="checkbox" value="java" v-model="technology" id="java"/>

<label for="php">PHP</label>
<input type="checkbox" value="php" v-model="technology" id="php"/>


<label for="Python">Python</label>
<input type="checkbox" value="Python" v-model="technology" id="Python"/>
<!----------------------------Checkboxes Ended------------>
<br/>
<br />
<!----------------------------Radio Buttons started----------------->
<h4> Who I am</h4>

<label for="student">Student</label>
<input type="radio" value="student" v-model="professional" name="professional" id="student"/>

<label for="developer">Developer</label>
<input type="radio" value="developer" v-model="professional" name="professional" id="developer"/>
<br/>
<br />

<h4>Selected Technology{{ technology }}</h4>
<h4>I am a {{ professional }}</h4>
<!-----------------------------Radio Buttons started----------------->
  </div>
<!----------------If Else----------------->
  <h4 v-if="show">If  Condition</h4>
  <h4 v-else>Else  Condition</h4>
 
  <!---------toggle Content when button is clicked-------->
 <button v-on:click="show=!show">Toggle</button>
</template>

<script>
export default {

  /////////////component named as HelloWorld/////////////
  name: 'HelloWorld',

  data(){
    return {

      ////////////////Objects //////////////
      email:'',
      password:'',
      technology:[],
      professional:'',
      show:true

    }
  },
//////////Methods/////////////////
  methods:{
   getData(){
    console.warn("Values:",this.email,this.password)
   }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

