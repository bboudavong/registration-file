# registration-file
Simple code from FreeCodeCamp. I made some adjustments in CSS
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" type="text/css" href="forms.css" />
    <title>Free Code registration Form</title>
  </head>
  <body>
    
    <div class="heart"></div>

    <h1>Registraton Form</h1>
    <p>Please fill out this form with the required information</p>
    <form action="https://fcc-registration-form.com" />

    <form>
      <fieldset>
        <label>Enter Your First Name: <input type="text"  name="first-name" required /></label>
        <label>Enter Your Last Name: <input type="text" name="last-name" required /></label>
        <label>Enter Your Email: <input type="email" name="email" required /></label>
        <label>Create a New Password: <input type="password" name="password" pattern="[a-z0-5]{8,}" required /></label>
      </fieldset>
      
      <fieldset>
        <label>
          <input type="radio" name="account-type" class="inline" /> Personal Account</input>
        </label>
        <label>
          <input type="radio" name="account-type" class="inline" /> Business Account</input>
        </label>
        <label>
          <input type="checkbox" name="terms" class="inline" required> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a></input>
        </label>
      </fieldset>

      <fieldset>
        <label>Upload a profile picture:<input type="file" name="file"/>
          <label>Input your age (years):<input type="number" min="13" max="120" name="age"></input>
        </label>

        <label>How did you hear about us?
          <select name="referrer">
            <option value=""></option>>(select one)</option>
            <option value="1"></option>>YouTube</option>
            <option value="2"></option>>Facebook</option>
            <option value="3"></option>>Instagram</option>
            <option value="4"></option>>Other</option>
          </select>
        </label>
        <label>Provide a bio:<textarea rows="3" cols="30" placeholder="I enjoy long walks on the beach..." name="bio"></textarea></label>
      </fieldset>
      <input type="submit" value="Submit" class="Submit"> </input>
    </form>
  </body>
</html>



!--CSS--


body {
  width: 100%;
  height: 100vh;
  margin: 0;
  background: linear-gradient(35deg, #ccffff, #f0d4d4);
  color: #7bb5f3;
  font-family: Chalkduster, fantasy;
  font-size: 16px;
}

h1,p{
  margin: 1em auto;
  text-align: center;
  }

  form{
    margin: 0 auto;
    max-width: 500px;
    min-width: 300px;
    width: 60vw;
    padding: 2em;
    }

    fieldset{
      border: 0;
      padding-right: 0;
      padding-left: 0;
      padding-top: 2rem;
      padding-bottom: 2rem;
    }

    fieldset:not(:last-of-type){
      border-bottom: 3px solid #f0525ffb;
    }

    input, textarea, select{
      margin: 10px;
      width: 100%;
      margin-bottom: 0;
      margin-left: 0;
      margin-top: 10px;
      margin-right: 0;
      min-height: 2em;
    }

    .inline {
      width: unset;
      margin: 0 0.5em 0 0;
      vertical-align: middle;
    }

    input[type="submit"]{
      display: block;
      width: 60%;
      form: center;
      margin: 0 auto;
      height: 2em;
      font-size: 1.1rem;
      background-color: #edd1ee;
      border-color: white;
      min-width: 1em;
      margin-top: 1em;
      margin-bottom: 1em;
      }

    
      input, textarea {
      background-color: #edd1ee;
      border: 1px solid #edd1ee;
      color: #f77d7d;
  

      }

    
      input[type='file']{
      padding: 1px 2px;
      }

      Label {
      display: block;
      margin: 0.5rem 0;
      }

      .Submit {
      border-radius: 5px;
      color: rgba(231, 29, 29, 0.192);
      background-color:rgba(240, 227, 227, 0.192)
      padding: 5px 10px 8px 10px;
    }

      a{
      color: #eea0e1;
       }

  
.Submit:hover{
  animation-name: background-color bounce;
    animation-duration: 500ms;
}

@keyframes background-color{
  100%{
    background-color: skyblue;
}



}

.heart {
  position: absolute;
  margin: auto;
  top: 0;
  right: 0;
  bottom: 400px;
  left: 0;
  background-color: pink;
  height: 50px;
  width: 50px;
  transform: rotate(-45deg);
  animation-name: beat;
  animation-duration: 1s;
  animation-iteration-count: infinite;

}
.heart:after {
  background-color: pink;
  content: "";
  border-radius: 50%;
  position: absolute;
  width: 50px;
  height: 50px;
  top: 0px;
  left: 25px;
}
.heart:before {
  background-color: pink;
  content: "";
  border-radius: 50%;
  position: absolute;
  width: 50px;
  height: 50px;
  top: -25px;
  left: 0px;
}

@keyframes backdiv {
  50% {
    background: #ffe6f2;
  }
}

@keyframes beat {
  0% {
    transform: scale(1) rotate(-45deg);
  }
  50% {
    transform: scale(0.6) rotate(-45deg);
  }
}
