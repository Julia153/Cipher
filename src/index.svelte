<script>
    let input = ''
    let output = ''

    function encrypt() {
        console.log(`encrypt button clicked...`)
        let plaintext = input
        let ciphertext = ''

        for (let i = 0; i < plaintext.length; i++) {
            ciphertext += plaintext.charCodeAt(i) + '|'

        }
    output = ciphertext
    }

    function decrypt() {
        console.log(`decrypt button was clicked ...`)
        let ciphertext = input
        let plaintext = ''
        let charCode = ''

        for (let i = 0; i < ciphertext.length; i++) {
            if (ciphertext[i] !== '|') {
                charCode += ciphertext[i]
            } else {
                plaintext += String.fromCharCode(charCode)
                charCode = ''
            }
        }
        output = plaintext
    }
</script>
<section class="section content">
    <h1>Cipher</h1>

    <label>
    <input type="text" bind:value={input}>
    </label>
    <button class="button" on:click={encrypt }>Encrypt</button>
    <button class="button" on:click={decrypt}>Decrypt</button>
    <h2>Result</h2>
    <p>{output}</p>
</section>
