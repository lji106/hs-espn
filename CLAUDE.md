# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is **Shepaug Valley High School ESPN** — an ESPN-style sports statistics website for Shepaug Valley High School (Washington, CT). School team: Spartans. Colors: navy blue (`#1a2a5e`) and white (`#fff`).

The site covers 15 teams across three seasons:
- **Fall:** Golf, Boys Soccer, Girls Soccer, Boys Cross Country, Girls Cross Country, Field Hockey
- **Winter:** Girls Basketball, Ice Hockey, Indoor Track
- **Spring:** Baseball, Softball, Boys Track & Field, Girls Track & Field, Boys Tennis, Girls Tennis

## Current State

The project is in early development. There is currently **one file**: `index.html` — a static homepage with the navy/white theme, a hero section, and team cards grouped by season. No build system, no dependencies, no backend yet.

## Planned Tech Stack

1. **HTML/CSS/JavaScript** — static pages (current phase)
2. **Supabase** — Postgres database + auth (free tier), for storing stats, rosters, schedules
3. **GitHub** — version control
4. **Vercel** — hosting/deployment

## Design Conventions (established in index.html)

- Background: `#0a0e1a` (near-black)
- Primary navy: `#1a2a5e`
- Accent blue for season titles: `#7a9fd4`
- Muted text: `#aaa`
- Font: Arial, sans-serif
- All CSS is written inline in `<style>` tags (no external stylesheet yet)
- Team cards use `.team-card` with hover state (`background-color: #1a2a5e`, `border-color: #fff`)

## Planned Page Structure

Each team will need its own page with:
- Team record + stats
- Schedule / upcoming games
- Roster with links to individual player pages

Each player page will show sport-specific stats (e.g. points/rebounds for basketball, batting avg for baseball, win/loss for tennis). The database schema needs to handle sport-specific stat fields across 15 different sports.

## Development

No build step — open `index.html` directly in a browser or use VS Code Live Server. No package manager or test runner is configured yet.

## End of Session Protocol

At the end of every working session, run a `git add . && git commit && git push` to save all progress to GitHub. A session is over when the user says something like "done for today", "good work", "see you later", or the exact phrase **"Good work today"**.
