## About

A Claude skill that generates a detailed, formal executive briefing document to help an account executive to quickly get a point of view on how they can help an account they are tareting. Just provide a company name, website URL, your job title, and company — Claude handles the research and formatting.

## What it does

Produces a 5–7 page briefing covering company overview, leadership, culture, competitive landscape, business risks, a Challenger Sale point of view, and additional resources for deeper analysis (podcasts, keynotes, blog posts, recent news).

## Usage

1. Copy the prompt below into Claude (or wherever you keep reusable skills).
2. Fill in `<current job title>` and `<current employer>` with your own details.
3. Provide the target company's name, URL, and a link to the job description.
4. Claude will generate the brief as a Word document (`.docx`) named `<Company Name> Executive Brief`.

## Skill


# Account Briefing Report — Claude Skill

A [Claude Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) that generates a formal, research-backed account briefing document for enterprise sales — the kind of pre-call research you'd do before selling into a target company. Originally built for enterprise technology sales (cloud/infrastructure), but the structure generalizes to any B2B sales motion.

Given a job title, your company, and a target account name + URL, Claude will:

1. Research the target account using web search (company site, SEC filings/annual reports, earnings calls, executive interviews, trade press)
2. Produce a formal Word document (`.docx`) covering company overview, financials, leadership, product set, competitive landscape, business risks, stated corporate goals, and a tailored "challenger sale" point of view on how your company can create value for that account
3. Wrap up with curated additional resources (podcasts, keynotes, recent news)

## Example output

Ideal length is 5–7 pages (soft cap of 15). Sections are fully structured with headings, and the "Our Value Offer" section is broken into per-initiative subsections (Problem/Goal, Our Solution, Value, Key Personas, Sales Strategy & Cycle) so it reads like a real internal sales brief, not a Wikipedia summary.

## Installation

### Claude.ai / Claude apps
Download `SKILL.md` (or the packaged `.skill` file, if you build one — see below) and add it via **Settings → Capabilities → Skills** (or the in-conversation "Save skill" prompt if a teammate shares it with you in a chat).

### Claude Code / API
Copy the `SKILL.md` folder into your skills directory (e.g. `.claude/skills/` for a project, or your global skills path). See [Anthropic's Skills documentation](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) for the exact path conventions for your setup.

## Usage

Just ask Claude for account research, e.g.:

> "I need an account brief for Acme Corp — I'm an Account Executive at MyCompany, acmecorp.com"

Claude will ask for anything it's missing (your job title, your company, the target account + URL) before starting research, then generate and hand you a downloadable `.docx`.

## Requirements

- Web search capability (for research)
- File creation / `.docx` generation capability (Claude.ai's file creation feature, or an equivalent tool in your environment)

## Customizing

The mandatory section list and the "challenger mentality" framing in `SKILL.md` are meant to be edited — fork this and adjust the sections, tone, or value-offer structure to match your own company's sales methodology (MEDDIC, Challenger, etc.).

## License

MIT — see [LICENSE](LICENSE).
