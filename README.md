# Aayush's Omnix AI Chatbot 🤖

This is my **personal AI Chatbot project**, built using **Next.js 14**, **Vercel AI SDK**, and **Google Gemini API**.  
It’s a modern open-source chatbot web app designed for fast, interactive, and intelligent conversations — featuring authentication, chat history, and a clean UI.

---

## 🚀 Features

- **Next.js App Router**
  - Fast navigation and optimized performance
  - Uses React Server Components (RSCs) and Server Actions for server-side rendering

- **AI SDK by Vercel**
  - Unified API for generating text, structured data, and tool calls with LLMs
  - Hooks for building dynamic chat and generative interfaces
  - Supports multiple providers like Google (default), OpenAI, Anthropic, and Cohere

- **Modern UI & Styling**
  - Built with **Tailwind CSS** and **shadcn/ui**
  - Accessible component primitives from **Radix UI**
  - Fully responsive and clean chat layout

- **Data Persistence**
  - **Vercel Postgres (powered by Neon)** for storing chat history and user data
  - **Vercel Blob** for efficient file/object storage

- **Authentication**
  - Secure user sign-in using **NextAuth.js**

---

## 🧠 Model Providers

The default model used is **Google Gemini (`gemini-1.5-pro`)**.  
However, thanks to the **AI SDK**, you can easily switch to other models such as:
- [OpenAI](https://openai.com)
- [Anthropic](https://anthropic.com)
- [Cohere](https://cohere.com)
- and many others available [here](https://sdk.vercel.ai/providers/ai-sdk-providers)

---

## ⚡ Deploy Your Own

You can deploy your own version of this chatbot instantly on **Vercel** 👇

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fvercel-labs%2Fgemini-chatbot&env=AUTH_SECRET,GOOGLE_GENERATIVE_AI_API_KEY&envDescription=Learn%20more%20about%20how%20to%20get%20the%20API%20Keys%20for%20the%20application&envLink=https%3A%2F%2Fgithub.com%2Fvercel-labs%2Fgemini-chatbot%2Fblob%2Fmain%2F.env.example&demo-title=Aayush%20AI%20Chatbot&demo-description=An%20AI%20Chatbot%20Built%20With%20Next.js%20and%20the%20Vercel%20AI%20SDK.&demo-url=https%3A%2F%2Fchat.vercel.ai&stores=[{%22type%22:%22postgres%22},{%22type%22:%22blob%22}])

---

## 🛠️ Running Locally

You’ll need the environment variables listed in [`.env.example`](.env.example).  
You can either use **Vercel Environment Variables** or a local `.env` file.

> ⚠️ Don’t commit your `.env` file — it contains private API keys and secrets.

### Steps to Run:

```bash
# 1. Install Vercel CLI
npm i -g vercel

# 2. Link your project
vercel link

# 3. Pull environment variables
vercel env pull

# 4. Install dependencies
pnpm install

# 5. Run the development server
pnpm dev
