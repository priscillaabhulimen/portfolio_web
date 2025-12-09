<template>
  <section id="contact" aria-labelledby="contact-heading" class="py-24 flex-col max-w-[80%] mx-auto">
    <h1 id="contact-heading" class="text-4xl font-serif mb-6">Contact</h1>

    <div class="flex flex-col gap-10">
      <form @submit.prevent="sendEmail" class="flex flex-col gap-6 w-full mx-auto">
      <label for="name" class="sr-only">Your Name</label>
      <input id="fullName" v-model="fullName" type="text" placeholder="Your Full Name"
        class="bg-white/10 border border-white rounded-sm p-3 w-full text-white placeholder-white/70 focus:outline-none focus:ring-2 focus:ring-blue-400"
        required>

      <label for="subject" class="sr-only">Email Subject</label>
      <input id="subject" v-model="subject" type="text" placeholder="Email Subject"
        class="bg-white/10 border border-white rounded-sm p-3 w-full text-white placeholder-white/70 focus:outline-none focus:ring-2 focus:ring-blue-400"
        required>

      <!-- Message Field -->
      <label for="message" class="sr-only">Your Message</label>
      <textarea id="message" v-model="message" placeholder="Your Message" rows="5"
        class="bg-white/10 border border-white rounded-sm p-3 w-full text-white placeholder-white/70 focus:outline-none focus:ring-2 focus:ring-blue-400"
        required></textarea>

      <!-- Submit Button -->
      <a @click="sendEmail"
        class="inline-block px-10 py-4 rounded-xl border border-white focus-visible:outline max-w-[200px] text-center"
        aria-label="Send Priscilla an email">
        Send Email
      </a>
    </form>

    <p> - OR - </p>
    
    <div>
      <p class="opacity-70 mb-4">
        You can view my Linkedin, github, Stack Overflow and more detailed information about me and my qualifications. Just click the link below
      </p>

      <a href="https://bento.me/priscilla-a" target="new"
        class="inline-block px-10 py-4 rounded-xl border border-white focus-visible:outline max-w-[200px] text-center"
        aria-label="Get all Priscilla's links in one place">
        See all my links
      </a>
    </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      subject: '',
      message: ''
    }
  },
  methods: {
    sendEmail() {
      const yourEmail = "priscillaabhulimen@gmail.com";
      const mailSubject = encodeURIComponent(`${this.name} - ${this.subject}`);
      const mailBody = encodeURIComponent(this.message);

      window.location.href = `mailto:${yourEmail}?subject=${mailSubject}&body=${mailBody}`;
    }
  }
}
</script>
