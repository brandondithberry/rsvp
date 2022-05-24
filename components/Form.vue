<template>
  <div class="form w-full">
    <form netlify name="invite" method="post" action="success" class="w-full mx-auto color-dark">
      <div class="w-full grid grid-cols-2 text-left gap-4">
        <div>
          <label for="firstname">First Name</label>
          <input id="firstname" type="text" name="firstname" required />
        </div>
        <div>
          <label for="lastname">Last Name</label>
          <input id="lastname" type="text" name="lastname" required />
        </div>
      </div>
      <div class="w-full grid grid-cols-1 text-left">
        <label for="email">Email</label>
        <input id="email" type="email" name="email" required />
        <label for="company">Company Name</label>
        <input id="company" type="text" name="company" required />
        <h4>
          We will require all attendees to show proof of vaccination or be
          tested on the day of the event.
        </h4>
        <label><input type="checkbox" name="vaccinated" value="vaccinated" /> Yes, I am fully vaccinated.</label>
      </div>
      <button class="btn" type="submit">Send RSVP</button>
    </form>
  </div>
</template>

<style lang="postcss" scoped>
.form {
  @apply flex w-full;
  margin: 0 auto;
}

.form .btn {
  width: 100%;
}

h4,
input[type='text'],
input[type='email'],
textarea {
  @apply inline w-full text-left py-3;
}

label,
span {
  @apply text-lg block py-2 m-0;
}

input[type='checkbox'] {
  @apply inline py-3;
}

input[type='checkbox']:after {
  background: #0060a9;
}

input[type='checkbox']:checked:before {
  background: #0060a9;
}

input[type='text'],
input[type='email'] {
  @apply border-primary border-2 p-2;
  box-shadow: 0px 0px 5px #0060a9, inset 0px 0px 5px #0060a9;
  background: #03001377;
  transition: all 0.4s ease;
  color: #fff;
}

input[type='text']:focus,
input[type='text']:focus-visible,
input[type='text']:active,
input[type='email']:focus,
input[type='email']:focus-visible,
input[type='email']:active {
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
