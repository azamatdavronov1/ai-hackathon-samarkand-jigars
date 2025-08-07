# ClarityScan - MRI/MRT AI Analysis App Architecture

## Overview
ClarityScan is a Flutter mobile application that analyzes MRI/MRT medical images using OpenAI's GPT-4o vision model to provide AI-powered diagnostic insights with accuracy assessments.

## Core Features
- Dark medical-themed UI matching the provided design
- Image upload from gallery with MRI/MRT validation warnings
- AI-powered image analysis using OpenAI GPT-4o
- Results display with confidence levels and recommendations
- Medical disclaimers and safety warnings
- Multi-language support (English, Russian, Uzbek placeholders)

## App Structure

### 1. Main App Entry (`main.dart`)
- App configuration with dark medical theme
- Routes to HomePage as initial screen

### 2. Theme System (`theme.dart`)
- Custom dark medical theme with appropriate colors
- Matches the provided design screenshot
- Uses Google Fonts (Inter) for typography

### 3. Screens
#### HomePage (`screens/home_page.dart`)
- Central "Medscan AI" branding
- Upload button with loading states
- Warning about MRI/MRT compatibility
- Terms and language selection

#### Analysis Results Page (`screens/analysis_result_page.dart`)
- Image preview of uploaded scan
- AI analysis results display
- Confidence percentage
- Medical findings and recommendations
- Beta warning and disclaimers
- New scan button to return home

### 4. AI Integration (`openai/openai_config.dart`)
- OpenAI GPT-4o integration for medical image analysis
- Structured JSON response parsing
- Error handling and fallbacks
- Medical-specific prompting

### 5. Data Models (`models/analysis_result_model.dart`)
- Structured data handling for analysis results
- JSON serialization/deserialization
- Validation methods

## Technical Dependencies
- `image_picker`: Image selection from gallery
- `http`: API communication with OpenAI
- `shared_preferences`: Local data persistence
- `google_fonts`: Typography consistency

## Platform Configurations
### Android Permissions
- Camera access for future camera functionality
- Storage read/write for image handling
- Internet access for AI API calls

### iOS Permissions
- Camera usage description
- Photo library access description
- App name updated to "ClarityScan"

## AI Analysis Flow
1. User selects MRI/MRT image from gallery
2. Image is converted to base64 format
3. Sent to OpenAI GPT-4o with medical analysis prompt
4. AI returns structured JSON with findings, confidence, recommendations
5. Results displayed with appropriate medical disclaimers

## Safety Features
- Prominent warnings about MRI/MRT compatibility
- Medical disclaimers on every analysis
- Beta warning emphasizing need for professional medical advice
- Terms of service acknowledgment

## UI/UX Principles
- Dark medical theme for professional appearance
- Clear visual hierarchy with appropriate spacing
- Loading states for better user experience
- Accessible design with proper contrast ratios
- Consistent Material Design 3 components