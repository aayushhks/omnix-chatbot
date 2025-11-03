# Aayush's Omnix AI Chatbot 🤖

This is my **personal AI Chatbot project**, built using **Next.js 14**, **Vercel AI SDK**, and **multiple AI providers**.  
It’s a modern open-source chatbot web app designed for fast, interactive, and intelligent conversations—featuring authentication, chat history, real-time tool usage, and a clean UI.

---

## 🚀 Features

- **Next.js App Router**
  - Fast navigation and optimized performance
  - Uses React Server Components (RSCs) and Server Actions

- **AI SDK by Vercel**
  - Easily switch between different AI models (Gemini, OpenAI, Grok).
  - Hooks for building dynamic chat and generative interfaces.

- **Real-Time API Integration**
  - Connects to the **Amadeus for Developers API** to fetch real-time flight data, replacing the original template's sample data.

- **Modern UI & Styling**
  - Built with **Tailwind CSS** and **shadcn/ui**.
  - Accessible component primitives from **Radix UI**.
  - Fully responsive and clean chat layout.

- **Data Persistence**
  - **Vercel Postgres** for storing chat history and user data.
  - **Vercel Blob** for file/object storage.

- **Authentication**
  - Secure user sign-in using **NextAuth.js**.

---

## 🧠 Model Providers

This chatbot is configured to use several different models. You can easily switch the active model in `app/(chat)/api/chat/route.ts`.

- **Google Gemini** (e.g., `gemini-1.5-pro`)
- **OpenAI** (e.g., `gpt-4o`)
- **Grok** (via their OpenAI-compatible API, e.g., `llama3-8b-8192`)
- **Anthropic, Cohere, and more** can be easily added via the Vercel AI SDK.

---

## ⚡ Deploy Your Own

You can deploy your own version of this chatbot instantly on **Vercel** 👇

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fvercel-labs%2Fgemini-chatbot&env=AUTH_SECRET,GOOGLE_GENERATIVE_AI_API_KEY,OPENAI_API_KEY,GROK_API_KEY,AMADEUS_CLIENT_ID,AMADEUS_CLIENT_SECRET&envDescription=API%20Keys%20needed%20for%20the%20chatbot%20to%20function.&demo-title=Aayush%20AI%20Chatbot&demo-description=An%20AI%20Chatbot%20Built%20With%20Next.js%20and%20the%20Vercel%20AI%20SDK.&demo-url=https%3A%2F%2Fchat.vercel.ai&stores=[{%22type%22:%22postgres%22},{%22type%22:%22blob%22}])

---

## 🛠️ Running Locally

You’ll need to create a `.env.local` file and add the following environment variables:

- **Auth:**
  - `AUTH_SECRET`: A random string for NextAuth.js.

- **Database & Storage:**
  - `POSTGRES_URL`: (Handled by `vercel env pull`)
  - `BLOB_READ_WRITE_TOKEN`: (Handled by `vercel env pull`)

- **AI Model Keys:**
  - `GOOGLE_GENERATIVE_AI_API_KEY`: Your Google AI Studio key.
  - `OPENAI_API_KEY`: Your OpenAI API key.
  - `GROK_API_KEY`: Your Grok API key.

- **Flight Data API:**
  - `AMADEUS_CLIENT_ID`: Your Amadeus API Key.
  - `AMADEUS_CLIENT_SECRET`: Your Amadeus API Secret.

> ⚠️ Don’t commit your `.env.local` file — it contains private API keys and secrets.

### Steps to Run:

```bash
# 1. Install Vercel CLI
npm i -g vercel

# 2. Link your project (and pull env variables)
vercel link
vercel env pull

# 3. Install dependencies
pnpm install

# 4. Run the development server
pnpm dev
