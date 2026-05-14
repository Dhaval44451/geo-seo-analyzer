# SEO + GEO Optimization Analyzer

A production-grade MVP web application for analyzing website SEO performance and AI/LLM visibility. Built with Next.js, Node.js, and modern tools.

## Features

- **SEO Score (0-100)**: Comprehensive evaluation of traditional SEO metrics
- **GEO Score (0-100)**: AI/LLM optimization for systems like ChatGPT, Claude, Gemini
- **Technical Health Score**: Page performance and technical implementation
- **AI Visibility Score**: Content readiness for generative AI systems
- **Detailed Analysis**: Title tags, meta descriptions, headings, schema markup, images, content depth
- **GEO Metrics**: Content chunking, FAQ presence, entity richness, E-E-A-T signals
- **AI-Powered Recommendations**: Context-specific fixes using OpenAI integration
- **Professional PDF Reports**: 5-page audit reports with actionable roadmaps
- **Issue Categorization**: Critical, Medium, and Minor issues with detailed context
- **Fast & Lightweight**: Real-time analysis with progress indicators

## Quick Start

1. **Install dependencies** (already done):
```bash
npm install
```

2. **Configure environment variables**:
Create `.env.local`:
```env
OPENAI_API_KEY=sk_your_openai_api_key_here
NEXT_PUBLIC_API_URL=http://localhost:3000
NODE_ENV=development
```

3. **Run development server**:
```bash
npm run dev
```

4. **Open** http://localhost:3000 in your browser

## Project Structure

```
seo-analyzer/
├── app/
│   ├── api/
│   │   ├── analyze/route.ts      # Main analysis API
│   │   └── report/route.ts       # PDF generation
│   ├── globals.css               # Tailwind styles
│   └── page.tsx                  # Main page
├── lib/
│   ├── utils/                    # URL validation & crawling
│   ├── analyzers/                # SEO, GEO, Scoring engines
│   ├── ai/                       # OpenAI integration
│   └── pdf/                      # PDF report generator
├── components/                   # React components
├── .env.local                    # Environment variables
└── README.md
```

## Usage

1. Enter website URL
2. Click "Start Analysis"
3. View results with scores and issues
4. Download professional PDF report

## API Endpoints

### POST `/api/analyze`
Analyzes a website and returns audit data.

**Request**: `{ "url": "https://example.com" }`

**Response**: Comprehensive analysis with scores, issues, and metrics.

### POST `/api/report`
Generates PDF report from analysis data.

## Analysis Metrics

### SEO Score (0-100)
- Title tags, meta descriptions, headings
- Schema markup, Open Graph tags
- Image alt text, content depth
- Internal/external links, canonicals

### GEO Score (0-100)
- Content chunking and structure
- Conversational readability
- FAQ presence and entity richness
- AI snippet readiness
- E-E-A-T signals (Expertise, Experience, Authority, Trust)

### Technical Score
- Page load time
- Essential tags presence
- Image optimization
- Link health

### AI Visibility Score
- AI content readiness
- Snippet extraction potential
- LLM-friendly structure

## Technologies

- **Frontend**: Next.js 14, TypeScript, Tailwind CSS
- **Backend**: Node.js, Next.js API Routes
- **Analysis**: Cheerio, Puppeteer
- **AI**: OpenAI API (Claude 3.5 Sonnet)
- **PDF**: jsPDF, html2canvas

## Building for Production

```bash
npm run build
npm run start
```

## Environment Variables

- `OPENAI_API_KEY` - OpenAI API key (required)
- `NEXT_PUBLIC_API_URL` - API base URL
- `NODE_ENV` - Environment type

## License

MIT License - Open source for educational and commercial use

---

**Version**: 1.0.0  
**Status**: Production Ready  
**Built with**: Next.js, TypeScript, Tailwind CSS, OpenAI

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
