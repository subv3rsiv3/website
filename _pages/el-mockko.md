---
layout: default
title: "El Mockko"
permalink: /el-mockko/
---

Here’s the tool that lets you mockify your text!

   <div class="el-mockko-container">
        <h2 style="text-align: center;">El Mockko - Text Alternator</h2>

       <!-- Input Text Area -->
   <label for="inputText">Enter Text:</label>
        <textarea id="inputText" rows="4" placeholder="Type your text here..."></textarea>

        <!-- Output Area -->
   <label for="outputText">Converted Text:</label>
   <input type="text" id="outputText" readonly>

        <!-- Action Buttons -->
   <button onclick="convertText()">Mockify</button>
   <button onclick="copyToClipboard()">Copy to Clipboard</button>

        <!-- Output Result Display -->
   <div id="output" class="el-mockko-result"></div>
    </div>

    <!-- JavaScript for Mockify and Clipboard functionality -->
<script>
   function convertText() {
        const input = document.getElementById('inputText').value;
        let mockified = '';
        let toggle = true;
            for (let i = 0; i < input.length; i++) {
                let char = input[i];
                if (char.match(/[a-z]/i)) {
                    mockified += toggle ? char.toLowerCase() : char.toUpperCase();
                    toggle = !toggle;
                } else {
                    mockified += char;
                }
            }
            document.getElementById('outputText').value = mockified;
            document.getElementById('output').textContent = mockified;
        }

        function copyToClipboard() {
            const text = document.getElementById('outputText');
            text.select();
            document.execCommand('copy');
            alert('Copied to clipboard!');
        }
</script>
