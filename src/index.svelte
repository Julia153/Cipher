<script>
    let input = ''
    let output = ''

    function encrypt() {
        console.log(`encrypt button clicked!`)
        let plaintext = input
        let ciphertext = ''

        for (let i = 0; i < plaintext.length; i++) {
            ciphertext += plaintext.charCodeAt(i) + '|'

        }
    output = ciphertext
    }
</script>
<section class="section content">
    <h1>Cipher</h1>

    <label>
    <input type="text" bind:value={input}>
    </label>
    <button class="button" on:click={encrypt }>Encrypt</button>
    <h2>Result</h2>
    <p>{output}</p>
</section>
