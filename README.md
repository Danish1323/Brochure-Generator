# 📄 AI Brochure Generator

Honestly, I got tired of clicking through a dozen "About Us" and "Services" pages just to figure out what a company actually *does*. So, I built this tool to do it for me.

It takes any website URL, scrapes the messy HTML, cleans it up, and feeds it into an LLM (GPT-4o) to generate a professional, one-page brochure in Markdown.

## 🤷‍♂️ Why I built this
I'm currently deep-diving into AI Engineering (following the Ed Donner track!), and I wanted to build something that wasn't just a basic chatbot. I wanted to see if I could connect **real-world data** (messy websites) with **AI reasoning**.

The hardest part wasn't the AI—it was cleaning up the raw HTML so the model wouldn't get confused by navigation bars and footer links.

## ⚙️ How it works
1.  **The Scraper (`scraper.py`):** I wrote a custom script using `BeautifulSoup` and `Requests` that grabs the website content. It filters out the noise (scripts, styles, images) and just keeps the relevant text.
2.  **The Brain (`project2.ipynb`):** The cleaned text is sent to OpenAI's GPT-4o-mini.
3.  **The Output:** The AI streams back a perfectly formatted brochure with the company's name, core value, and key features.

## 🛠️ Tech Stack
* **Python 3** (The glue holding it all together)
* **BeautifulSoup4** (For scraping the web)
* **OpenAI API** (The intelligence)
* **IPython Display** (To render the Markdown in real-time)

## 🚀 How to run it on your machine

1.  **Clone this repo:**
    ```bash
    git clone [https://github.com/Danish1323/Brochure-Generator.git]
    cd Brochure-Generator
    ```

2.  **Install the dependencies:**
    ```bash
    pip install openai beautifulsoup4 requests python-dotenv
    ```

3.  **Set up your keys:**
    Create a `.env` file in the main folder and add your OpenAI key:
    ```env
    OPENAI_API_KEY=sk-your_key_here
    ```

4.  **Run the notebook:**
    Open `brochure-gen.ipynb` in Jupyter or VS Code, change the URL in the last cell to whatever company you want to research, and hit run!

## 🔮 What's next?
I'm planning to upgrade this by:
* Adding a proper frontend (maybe Streamlit or Gradio).
* Making it handle multiple pages (not just the homepage).
* Dockerizing it so it's easier to deploy.

---
*Built by Danish while learning AI Engineering.*
