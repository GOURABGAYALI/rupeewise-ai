# RupeeWise AI — Inflation Intelligence

A responsive inflation-impact calculator with an optional Gemini-powered explanation via a serverless function. The calculator and built-in demo insight work without an API key.

## Free deployment on Netlify
1. Create a free account at https://www.netlify.com/.
2. Put the contents of this folder in a GitHub repository, then in Netlify choose **Add new site → Import an existing project** and connect the repository. The serverless function needs to be deployed with the rest of the project; a static-only drag-and-drop preview will not run live AI.
3. Get a Gemini API key at https://aistudio.google.com/app/apikey (review current pricing and free-tier limits at https://ai.google.dev/gemini-api/docs/pricing).
4. In Netlify site environment variables, set `GEMINI_API_KEY` to your key and redeploy.
5. Open the published URL. The **Generate AI insight** button will call the serverless function.

Never put the API key in `index.html` or commit it to GitHub. Free tiers and limits can change.

## Technology and project explanation
- Front end: HTML, CSS, JavaScript, responsive layout and SVG chart.
- Formula: future cost = current amount × (1 + inflation rate)^years; purchasing power in today's rupees = current amount ÷ (1 + inflation rate)^years.
- AI: Gemini generates a plain-English explanation through a Netlify serverless function, keeping the API key off the client.
- Purpose: financial literacy and educational estimates, not investment advice.
