<template>
  <div class="form w-full">
    <form name="invitation" netlify data-netlify="true">
      <div class="grid grid-cols-2 gap-4">
        <input type="hidden" name="form-name" value="invitation">
        <label>First Name <input type="text" name="firstname" /></label>
        <label>Last Name <input type="text" name="lastname" /></label>
      </div>
      <div>
        <label>Email <input type="email" name="email" /></label>
      </div>
      <div class="mt-4">
        <h4 class="block mt-4">We will require all attendees to show proof of vaccination or be tested on the day of the event.</h4>
        <h3>Are you fully vaccinated?</h3>
        <label><input type="radio" name="vaccinated"> Yes, I am fully vaccinated.</label>
        <label><input type="radio" name="notvaccinated"> No, I am not fully vaccinated.</label>
      </div>
      <button class="btn" type="submit">Send RSVP</button>
    </form>
  </div>
</template>

<style lang="postcss" scoped>
.form {
  @apply flex w-full text-left;
  margin: 1rem auto 0 auto;
}

.form .btn {
  width: 100%;
}

.form h4,
.form input[type='text'],
.form input[type='email'] {
  @apply inline w-full py-3;
}

.form label {
  @apply text-lg block py-2 m-0;
}

.form  input[type='checkbox'] {
  @apply inline py-3;
}

.form input[type='checkbox']:after {
  background: #0060a9;
}

.form input[type='checkbox']:checked:before {
  background: #0060a9;
}

.form input[type='text'],
.form input[type='email'] {
  @apply border-primary border-2 p-2;
  box-shadow: 0px 0px 5px #0060a9, inset 0px 0px 5px #0060a9;
  background: #03001377;
  transition: all 0.4s ease;
  color: #fff;
}

.form input[type='text']:focus,
.form input[type='text']:focus-visible,
.form input[type='text']:active,
.form input[type='email']:focus,
.form input[type='email']:focus-visible,
.form input[type='email']:active {
  border-color: #acf2fd;
  box-shadow: 0px 0px 10px #acf2fd, inset 0px 0px 5px #acf2fd;
}

.hidden {
  clip: rect(0 0 0 0);
  clip-path: inset(50%);
  height: 1px;
  overflow: hidden;
  position: absolute;
  white-space: nowrap;
  width: 1px;
}
</style>
