<script setup>
/* Zander Spies u25033931 */
    useHead
    (
        {
            title: "Contact"
        }
    )
</script>

<template>
  <section class="contact-section">
    <h2>Contact Me</h2>
    <p>Have a question or want to work together? Drop a message below!</p>

    <form 
      name="contact" 
      method="POST" 
      data-netlify="true" 
      data-netlify-honeypot="bot-field"
      netlify
    >
      <input type="hidden" name="form-name" value="contact" />
      <p class="hidden" style="display:none">
        <label>Don’t fill this out if you’re human: <input name="bot-field" /></label>
      </p>

      <div class="form-group">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required placeholder="Your Name" />
      </div>

      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required placeholder="your.email@example.com" />
      </div>

      <div class="form-group">
        <label for="message">Message:</label>
        <textarea id="message" name="message" required rows="5" placeholder="How can I help you?"></textarea>
      </div>

      <button type="submit" class="submit-btn">Send Message</button>
    </form>
  </section>
</template>

<style scoped>
    .contact-section 
    {
    max-width: 600px;
    margin: 0 auto;
    padding: 2rem;
    padding-top: 0px;
    }

    .form-group 
    {
    margin-bottom: 1.5rem;
    display: flex;
    flex-direction: column;
    }

    label 
    {
    margin-bottom: 0.5rem;
    font-weight: bold;
    }

    input, textarea
    {
    padding: 0.75rem;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-family: inherit;
    }

    .submit-btn
    {
    background-color: #42b883;
    color: white;
    padding: 0.75rem 1.5rem;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-weight: bold;
    transition: background-color 0.3s;
    }

    .submit-btn:hover
    {
    background-color: #35495e;
    }
</style>