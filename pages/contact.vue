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
        <h2 class="center">
          Kansas Wrestling Center
        </h2>
        <br><br><br>
        <p>1671 E Kansas City Rd</p>
        <p>Olathe, KS 6606</p>
        <br><br><br>
        <p>(913)555-0122</p><br>
        <p>(913)555-0123 (fax)</p>
        <br><br><br><br>
        <p>contact@kswrestlingcenter.com</p>
      </div>
      <div id="aside2" class="aside2">
        <form id="form">
          <h2>Contact Form</h2>
          <br>
          <div>
            <label>First Name</label>
            <input type="text" name="firstName" placeholder="Enter first name">
          </div>
          <div>
            <label>Last Name</label>
            <input type="text" name="lastName" placeholder="Enter last name">
          </div>
          <div>
            <label>Email</label>
            <input type="email" name="email" placeholder="champ@wrestleDB.com">
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
            <button type="submit" name="submit">
              Submit
            </button>
          </div>
        </form>
      </div>
    </div></div>
    <div class="clr" />
  </div>
</template>
