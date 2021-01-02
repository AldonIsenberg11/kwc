<template>
  <div class="container">
    <div id="contactpage">
      <h2>Contact Us</h2>
      <hr>
      <br>
      <br>
      <div id="contactbox">
        <div id="homeside2" class="center">
          <br><br><br><br>
          <h5 class="center">
            Kansas Wrestling Center
          </h5>
          <br>
          <iframe
            class="google-map"
            src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d12421.17655703115!2d-94.7903587!3d38.8943885!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x892dbb21abb0db5a!2sKansas%20Wrestling%20Center!5e0!3m2!1sen!2sus!4v1609184702742!5m2!1sen!2sus"
            width="400"
            height="300"
            frameborder="0"
            style="border: 0"
            allowfullscreen=""
            aria-hidden="false"
            tabindex="0"
          />
          <br><br><br>
          <p>1671 E Kansas City Rd</p>
          <p>Olathe, KS 66061</p>
          <br><br><br>
          <p>(719)322-2718</p>
          <br><br><br>
          <p>linda@kswrestlingcenter.com</p>
        </div>
        <div id="aside2" class="aside2">
          <form id="form">
            <h2>Contact Form</h2>
            <br>
            <div>
              <label>First Name</label>
              <input type="text" name="firstName" placeholder="Enter first name"></input>
            </div>
            <div>
              <label>Last Name</label>
              <input type="text" name="lastName" placeholder="Enter last name"></input>
            </div>
            <div>
              <label>Email</label>
              <input type="email" name="email" placeholder="champ@email.com"></input>
            </div>
            <div>
              <label>Subject</label>
              <select name="Subject">
                <option value="General">
                  General Question
                </option>
                <option value="Host">
                  Host an event
                </option>
                <option value="Facility">
                  Facility Info
                </option>
              </select>
            </div>
            <div>
              <textarea name="Message" placeholder="Your message here" />
            </div>
            <div class="button">
              <v-btn> Submit </v-btn>
            </div>
          </form>
        </div>
      </div>
    </div>
    <div class="clr" />
  </div>
</template>
