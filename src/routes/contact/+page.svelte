<script>
    let name = '';
    let email = '';
    let message = '';

    const handleSubmit = async (event) => {
        event.preventDefault();
        // Handle form submission logic here
        console.log({ name, email, message });
        alert('Form submitted successfully!');
    };
</script>

<style>
    form {
        max-width: 600px;
        margin: 0 auto;
        padding: 1rem;
        border: 1px solid #ccc;
        border-radius: 5px;
    }
    label {
        display: block;
        margin-bottom: 0.5rem;
    }
    input, textarea {
        width: 100%;
        padding: 0.5rem;
        margin-bottom: 1rem;
        border: 1px solid #ccc;
        border-radius: 5px;
    }
    button {
        padding: 0.5rem 1rem;
        background-color: #007BFF;
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
    }
    button:hover {
        background-color: #0056b3;
    }
</style>

<form on:submit={handleSubmit}>
    <label for="name">Name:</label>
    <input type="text" id="name" bind:value={name} required />

    <label for="email">Email:</label>
    <input type="email" id="email" bind:value={email} required />

    <label for="message">Message:</label>
    <textarea id="message" bind:value={message} required></textarea>

    <button type="submit">Submit</button>
</form>