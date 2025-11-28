AI Agent (Python)

Dit project is een simpele AI-assistent in de terminal, gebouwd in Python.
De agent gebruikt LangChain en LangGraph om een OpenAI-chatmodel aan te sturen
en kan eenvoudige "reason + act"-taken uitvoeren met behulp van tools.

Wat de agent doet
- Start in de terminal en toont een welkomstbericht.
- De gebruiker kan berichten typen en de agent antwoordt.
- De chat loopt door in een lus totdat de gebruiker "quit" typt.
- De agent heeft eenvoudige tools, zoals:
  - een rekenmachine-tool om twee getallen op te tellen
  - een say_hello-tool om een gebruiker te begroeten

Hoe het ongeveer werkt (in mensentaal)
- Een .env-bestand bevat de geheime OpenAI API-key.
- Met dotenv wordt die API-key beschikbaar gemaakt voor de Python-code.
- LangChain en LangGraph bouwen rond het OpenAI-model een "agent" die:
  - het gebruikersbericht leest,
  - kan beslissen of er een tool gebruikt moet worden,
  - de tool aanroept (bijv. calculator of say_hello),
  - en daarna een antwoord terugstuurt naar de gebruiker.
- In de main.py zit een while-loop die:
  - de input van de gebruiker leest,
  - het bericht doorstuurt naar de agent,
  - het antwoord van de agent in de terminal toont,
  - stopt zodra de gebruiker "quit" typt.

Benodigdheden
- Python en een werkende ontwikkelomgeving.
- Een .env-bestand met een geldige OpenAI API-key.
- Een terminal (bijvoorbeeld uv terminal of een gewone command prompt) om het script uit te voeren.

Beperking
Op dit moment heb ik zelf geen krediet op mijn OpenAI-account.
Dat betekent dat de agent in de terminal geen echt antwoord kan teruggeven
zolang er geen tegoed aan de gebruikte API-key is gekoppeld.
Bij onvoldoende quota zal de OpenAI-API een foutmelding geven en stopt het antwoord van de agent.
