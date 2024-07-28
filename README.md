<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Bold First Letters</title>
</head>
<body>
    <textarea id="inputText" rows="10" cols="50">This is a sample text to demonstrate the functionality of the script.</textarea>
    <br>
    <button onclick="boldFirstLetters()">Bold First 3 Letters</button>
    <div id="outputText"></div>

    <script>
        function boldFirstLetters() {
            let text = document.getElementById('inputText').value;
            let words = text.split(' ');
            let numLetters = 3;
            let boldedText = words.map(word => {
                if (word.length > numLetters) {
                    return `<b>${word.slice(0, numLetters)}</b>${word.slice(numLetters)}`;
                } else {
                    return `<b>${word}</b>`;
                }
            }).join(' ');

            document.getElementById('outputText').innerHTML = boldedText;
        }
    </script>
</body>
</html>
