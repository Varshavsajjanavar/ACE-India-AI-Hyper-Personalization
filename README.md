

# ACE India — Emotion-Aware Food Intelligence Layer

AI-powered contextual food recommendations inspired by Korea’s hyper-personalized food delivery ecosystem.

## Overview

Indian food delivery apps rely heavily on past orders, generic popularity, and discounts. However, they do not understand the user’s real-time emotional and situational context.

ACE India is a working prototype that brings Korean-style AI hyper-personalization to the Indian food ecosystem by combining:

* Emotion signals (mood)
* Weather
* Diet type
* Party size
* Price sensitivity
* User preferences
* Trending dishes

The system recommends the top 5 emotionally contextual dishes along with explanations such as:

* “Perfect for rainy weather”
* “Comfort food since you’re tired”
* “Matches your veg preference”
* “Trending today in your city”

## Target Users

ACE India is designed for:

### Food Delivery Platforms

To improve:

* Conversion rate
* User retention
* Average Order Value (AOV)
* Brand differentiation

### Restaurant Partners

To gain:

* Hyper-local insights
* Context-aware visibility
* Intelligent menu promotions

### End Users (Consumers)

Who expect:

* Smarter, personal, emotion-friendly food suggestions
* A feeling that “this app gets me”

## Core Idea

Korean food delivery platforms such as Baemin, Yogiyo, and Coupang Eats personalize food recommendations based on:

* Mood
* Weather
* Diet
* Time of day
* Local micro-trends
* Party size
* Health goals

Indian platforms have not yet implemented this deeper layer of emotional and situational personalization. ACE India fills this gap by adding emotion-aware intelligence on top of standard recommendation systems.

## System Architecture

### Input Signals

* mood
* weather
* diet
* party_size
* price_sensitivity
* user_id

### AI Pipeline

#### Semantic Understanding (Embeddings)

Model: SentenceTransformer MiniLM
Converts dish descriptions into meaning-aware vectors.

Examples:

* “Rasam → comfort food”
* “Hot chocolate → warmth”

#### Retrieval Layer

FAISS-based vector search
Retrieves dishes most relevant to the user’s real-time context.

#### Ranking Layer

LightGBM ranking model
Scores and ranks dishes based on factors such as:

* Mood–category alignment
* Weather–food match
* Veg/non-veg preference
* Price fit
* User taste patterns
* Local trending score
* Party size relevance

#### Explanation Engine

Generates clear, simple reasoning for every recommendation delivered to the user.

## Tech Stack

| Component      | Technology                          |
| -------------- | ----------------------------------- |
| Embeddings     | SentenceTransformer MiniLM          |
| Vector Search  | FAISS                               |
| Ranking        | LightGBM                            |
| Backend        | Python + FastAPI                    |
| Demo Hosting   | Ngrok                               |
| Infrastructure | CPU-friendly, low-cost, open-source |

## Features

* Real-time mood and weather-aware recommendations
* Explanation provided for each suggested dish
* High-speed retrieval using FAISS
* Lightweight architecture suitable for CPU environments
* Simple integration into existing food delivery systems
* Scalable to millions of dishes and user profiles

## Impact and Why It Matters

### Higher Conversion Rate (10–18%)

Emotion-aware suggestions increase ordering likelihood.
Examples:
Rain → soups, pakoras, chai
Tired → rasam, khichdi, warm foods

### Increased AOV

Contextual upselling includes:
Party size 3+ → combos
Rainy weather → snacks plus chai
Gym users → protein bowls

### Stronger Retention

Users return more often when the app delivers emotionally relevant and personalized suggestions.

### Brand Differentiation

Creates a competitive advantage similar to Korean food delivery ecosystems.

### Hyper-local Intelligence

Learns eating patterns and trends across specific local clusters such as:

* Offices
* Colleges
* Neighborhoods




