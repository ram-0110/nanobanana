# Consept_Art_Generator: Automated Cinematic Concept Art Generator

## Overview

NanoBanana is an AI-powered Jupyter Notebook that converts raw film scripts into cinematic concept art and storyboards. It dynamically injects character designs per scene to maintain visual consistency, automating the pre-visualization stage of filmmaking.

## Key Features

- **Script Analysis:** Extracts characters, scenes, and contextual details using NLP
- **Dynamic Scene Generation:** Creates detailed prompts with cinematic shots and emotional subtext
- **Character Consistency:** Injects predefined character designs ensuring visual coherence
- **Storyboard Compilation:** Generates images ready for PDF compilation

## Prerequisites

- OpenAI API access (for GPT analysis)
- Stability.ai or Midjourney API key (for image generation)
- Python 3.8+ environment

## Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/ram-0110/nanobanana.git
cd nanobanana
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. API Configuration

- Create `.env` file in root directory
- Add your API keys:

```
OPENAI_API_KEY=your_openai_key_here
STABILITY_KEY=your_stability_key_here
```

### 4. Character Assets Preparation

- Place character reference images in `/character_refs/` folder
- Naming convention: `CharacterName.jpg` (e.g., `Alice.jpg`)

## Example files
### Drive link
use this for script and images
https://drive.google.com/drive/folders/1GeomwG82Ra0YtIgd3fxg1FPLKrzsv4CC?usp=sharing




## Usage

### 1. Launch Notebook

```bash
jupyter notebook main.ipynb
```

### 2. Execution Steps

- Load your script in the first cell
- Run all cells sequentially
- After character extraction (Cell 3), verify:
  - All named characters have corresponding images in `/character_refs/`
  - Add missing character references before proceeding

### 3. Output

- Generated scenes save to `/output/scenes/`
- Final storyboard compiles to `/output/storyboard.pdf`

## Important Notes

- Character images must match exactly the names extracted from script
- Processing time varies based on script length (approx 2-3 minutes/scene)
- For best results use 1024x1024 PNG character references

## Troubleshooting

- **Missing characters:** Add corresponding images to `/character_refs/` and restart notebook
- **API errors:** Verify API keys in `.env` and quota status
- **Generation failures:** Check internet connection and API service status
