# Cognitive-web-agents


Core Flow & Logic Recap

User registers/login ✅



User can create a bot by providing a name + URL

Website content is scraped (BeautifulSoup)

Text is cleaned + split into chunks

Sentence embeddings generated via all-MiniLM-L6-v2

FAISS index built + saved to disk

Text chunks saved via pickle

Bot metadata (name, owner, URL, vector index path) saved in the bots table ✅



On chat request:

Fetch relevant bot metadata from DB

Load FAISS index + chunks

Search for similar text chunks

Build prompt for Gemini with context

Return Gemini’s response ✅

