# AI Chatbot (Spring 2023)

A simple emotional support chatbot that detects user's negative emotions and extreme behavior tendencies.

## Overview

This project implements a conversational AI that:
1. Engages in chat with users through natural language processing
2. Detects emotional state and extreme behavior tendencies
3. Provides simple mental health support when needed

## Core Functionality

### Emotion Analysis System
- Users input their thoughts/messages
- The input is sent to a pre-trained GPT-2 model for emotion scoring
- When emotional words (e.g., "sad", "angry") are detected:
  - Classifies the sentence as positive/negative
  - Adjusts the cumulative emotion score accordingly

### Extreme Behavior Detection
- Identifies potential extreme behavior tendencies in user inputs
- Maintains and adjusts an extreme behavior score

### Support Intervention System
1. **First Threshold Reached** (low emotion score or high behavior score):
   - Triggers a one-time MBSR (Mindfulness-Based Stress Reduction) therapy prompt
   - Asks if the user feels better:
     - If yes: Emotion score is halved
     - If no: Score remains unchanged

2. **Critical Threshold Reached** (very low emotion score or maximum behavior score):
   - Program concludes the session
   - Displays the calculated emotion and behavior scores
   - Provides a link to a depression self-assessment website with recommendations

## Technical Implementation
- User inputs are processed through:
  - ChatGPT-3 API for generating conversational responses
  - Pre-trained GPT-2 model for emotional analysis
- Scores are maintained throughout the conversation session
