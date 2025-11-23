# 1. Clone & enter (if repo exists)
git clone https://github.com/Muskan10975/RemedicaAI---Turning-Waste-into-Medicine-with-Generative-AI.git 
cd remedicaAI

# 2. Create virtual env
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt  # Includes langchain, openai, rdkit, pinecone-client, reportlab, etc.

# 4. Set environment variables
cp .env.example .env
# Edit .env: Add OPENAI_API_KEY=sk-..., ANTHROPIC_API_KEY=..., PINECONE_API_KEY=...

# 5. Run backend (if separate)
uvicorn app.py:app --reload  # Or streamlit run app.py for UI

# 6. For frontend-only (if HTML bundle)
# Open index.html in browser, or serve with: python -m http.server 8000
# Visit http://localhost:8000
