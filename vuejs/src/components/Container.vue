<template>
  <div class="main-container">
    <img
      src="https://admin.skavacommerce.com/admin/studio/customlib/img/loginBanner.jpg"
      alt=" Business related photo"
      class="business-picture"
    >
    <div class="form-wrapper">
      <h1 class="form-title">{{admintitle}}</h1>
      <form class="form-signin">
        <div icontype="mail" class="form-fields">
          <label class="form-label" for="maillabel">{{useremaillabel}}</label>
          <input type="text" id="maillabel" name="maillabel">
        </div>
        <div icontype="lock" class="form-fields">
          <label class="form-label" for="passowrdlabel">{{userpasswordlabel}}</label>
          <input type="password" id="passowrdlabel" name="passowrdlabel">
        </div>
        <div class="button-group">
          <div class="loggedin-wrapper">
            <div class="form-checkbox">
              <input checked type="checkbox" id="loggedin-checked">
              <label class="checkbox-support" for="loggedin-checked"></label>
            </div>
            <label class="loggedin-label" for="loggedin-checked">{{loginSavelabel}}</label>
          </div>
          <button class="form-button">{{submitlabel}}</button>
        </div>
        <a
          href="#"
          class="form-forgot-password"
          aria-label="get reset password"
        >{{forgotpasswordlabel}}</a>
      </form>
    </div>
  </div>
</template>


<script>
export default {
  name: "Footer",
  props: {},
  data: function() {
    return {
      admintitle: "Sign In",
      useremaillabel: "Your Email",
      userpasswordlabel: "Your Password",
      loginSavelabel: "Keep me logged in",
      submitlabel: "submit",
      forgotpasswordlabel: "Forgot Password?"
    };
  }
};
</script>

<style scoped>
.main-container {
  display: flex;
  flex-direction: row;
  background: white;
}
.main-container .business-picture {
  width: 50vw;
}
div.form-wrapper {
  width: 358px;
  margin: auto;
}
h1.form-title {
  font-size: 20px;
  color: #535353;
}
div.loggedin-wrapper {
  margin: auto 0;
  display: flex;
}
button.form-button {
  outline: none;
  font-size: 14px;
  color: white;
  background: #1c74bc;
  border: none;
  border-radius: 3px;
  height: 35px;
  padding: 0 60px;
  text-transform: capitalize;
}

.form-fields label {
  display: flex;
  margin-top: 30px;
  font-size: 14px;
  /* opacity: 0; */
}
.form-fields {
  display: flex;
  flex-direction: column;
  padding-left: 36px;
  position: relative;
  width: 100%;
}
.form-fields input {
  outline: none;
  border: none;
  width: 100%;
  border-bottom: 2px solid #ccc;
  height: 42px;
  font-size: 14px;
}
.form-fields input:focus {
  border-bottom: 2px solid #1c74bc;
}
.form-signin span {
  position: relative;
}
.form-signin .form-fields::after {
  content: attr(icontype);
  font-family: "Material Icons";
  font-weight: normal;
  font-style: normal;
  color: #292929;
  position: absolute;
  left: 0px;
  bottom: 9px;
  font-size: 20px;
}

.form-signin .button-group {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 50px 0 40px 0;
}
.loggedin-wrapper .loggedin-label {
  margin-left: 10px;
  line-height: 25px;
}
/* MEDIAQUREY CSS */

/* .form-checkbox */
.form-checkbox {
  width: 26px;
  height: 26px;
  position: relative;
  background: #1b75bc;
  border-radius: 3px;
}

.form-checkbox label.checkbox-support {
  width: 100%;
  height: 100%;
  cursor: pointer;
  position: absolute;
  left: 0;
  top: 0;
}
.form-checkbox label.checkbox-support:after {
  content: "";
  width: 9px;
  height: 5px;
  position: absolute;
  top: 8px;
  left: 7px;
  border: 3px solid #fcfff4;
  border-top: none;
  border-right: none;
  background: transparent;
  opacity: 0;
  transform: rotate(-45deg);
}
.form-checkbox label.checkbox-support:hover::after {
  opacity: 0.3;
}
.form-checkbox input[type="checkbox"] {
  visibility: hidden;
}
.form-checkbox input[type="checkbox"]:checked + label.checkbox-support:after {
  opacity: 1;
}
.form-signin .form-forgot-password {
  color: #1b75bc;
}
/* end .form-checkbox */

@media only screen and (max-width: 768px) {
  .main-container {
    flex-direction: column;
    position: relative;
  }
  .main-container:before {
    height: 230px;
    bottom: 0px;
    content: "";
    position: absolute;
    z-index: 0;
    width: 100%;
    background: -webkit-linear-gradient(
      top,
      rgba(255, 255, 255, 0) 0%,
      rgb(255, 255, 255) 83%,
      rgb(255, 255, 255) 85%
    );
  }
  .main-container .business-picture {
    width: 100vw;
    margin-bottom: 20px;
  }
  .main-container div.form-wrapper {
    width: 90vw;
    margin: auto;
    background: white;
    position: absolute;
    top: 40px;
    right: 0;
    left: 0px;
    height: auto;
    padding: 10px 27px 27px;
    max-width: 500px;
    box-shadow: 0px 8px 10px #00000033;
    z-index: 99;
  }

  .form-signin .button-group {
    flex-direction: column;
    margin-bottom: 0;
    margin-top: 20px;
  }
  .form-signin .button-group button {
    margin-top: 20px;
    margin-bottom: 20px;
  }
}
</style>
