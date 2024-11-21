<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Query Parameter Voorbeeld</title>
</head>
<body>
    <h1>Query Parameter Voorbeeld</h1>
    <div id="output"></div>

    <script>
        // Verkrijg de huidige URL
        const url = new URL(window.location.href);

        // Verkrijg de queryparameters
        const params = new URLSearchParams(url.search);

        // Lees de specifieke parameter 'name'
        const name = params.get('name');

        // Controleer of de parameter bestaat en toon de waarde op de pagina
        if (name) {
            document.getElementById('output').textContent = `De waarde van de naam is: ${name}`;
        } else {
            document.getElementById('output').textContent = 'Geen naam parameter gevonden.';
        }
    </script>
</body>
</html>
