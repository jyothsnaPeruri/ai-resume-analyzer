# AI Resume Analyzer Pro

An intelligent web-based resume analyzer powered by Google Gemini API. Get AI-driven insights on your resume's strengths, weaknesses, ATS compatibility, and generate professional cover letters.

## Features

✨ **Resume Analysis**
- Overall resume score (0-100)
- ATS (Applicant Tracking System) compatibility score
- Impact score assessment
- Identified key skills
- Strengths and improvement suggestions
- Professional summary

🎯 **Job Matching**
- Match resume against job descriptions
- Identify matched keywords and skills
- Highlight missing skills
- Get matching verdict

✍️ **Bullet Point Rewriting**
- AI-powered rewrite of resume bullets
- More impactful, action-oriented language
- Side-by-side comparison of before/after

📧 **Cover Letter Generation**
- Professional, personalized cover letters
- 4-5 paragraph business format
- Tailored to specific job roles
- One-click copy to clipboard

## How to Use

### Prerequisites
1. **Google Gemini API Key** (free)
   - Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
   - Click "Create API Key"
   - Copy your API key

2. **Web Browser** (Chrome, Firefox, Safari, Edge)

### Setup & Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/jyothsnaPeruri/ai-resume-analyzer.git
   cd ai-resume-analyzer
   ```

2. **Open in browser**
   - Simply open `index.html` in your web browser
   - Or use a local server:
     ```bash
     # Python 3
     python -m http.server 8000
     
     # Node.js (if http-server installed)
     npx http-server
     ```
   - Then visit: `http://localhost:8000`

3. **Add your API Key**
   - Paste your Gemini API key in the input field
   - Click "Save Key" (saved locally in browser)

4. **Analyze Your Resume**
   - Paste your resume text
   - Enter target job title
   - (Optional) Paste job description for matching
   - Click "Analyze Resume"
   - View results in different tabs

## Technologies Used

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **API**: Google Gemini 2.5-Flash API
- **Storage**: Browser localStorage for API key
- **No Dependencies**: Pure client-side app, no build tools needed

## File Structure

```
ai-resume-analyzer/
├── index.html          # Main application (all-in-one file)
├── README.md           # This file
└── .gitignore          # Git ignore file
```

## Key Features Explained

### Resume Analysis
Analyzes your resume for:
- Overall quality and impact
- ATS-friendly formatting score
- Key competencies extracted
- Specific strengths to highlight
- Areas for improvement

### Job Matching
Compares your resume against job requirements:
- Percentage match score
- Keywords that match the job
- Missing skills to acquire/highlight
- Recommendation on fit

### Bullet Rewriting
Transforms generic resume bullets into:
- Quantified achievements
- Action-driven statements
- Impact-focused language
- Industry-specific keywords

### Cover Letter
Generates professional cover letters with:
- Personalized opening
- Achievement highlights
- Skill alignment section
- Professional closing
- Business-appropriate tone

## API Limitations

- **Free tier**: Limited requests per minute
- **High demand**: May experience delays during peak times
- **Token limits**: Large resumes may be truncated
- **Recommended**: Use 200-500 word resumes for best results

If you get "Model experiencing high demand" error:
- Wait 5-10 minutes and try again
- Use a shorter resume
- Try during off-peak hours (early morning/late night)

## Security & Privacy

✅ **Your Data is Safe**
- API key stored locally in browser (not sent to any server)
- Resume data processed only by Google Gemini
- No data stored on our servers
- Clear API key anytime with "Clear Key" button

## Browser Compatibility

| Browser | Support |
|---------|---------|
| Chrome | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| Edge | ✅ Full |
| Opera | ✅ Full |

## Troubleshooting

**Q: "API key loaded successfully" but can't analyze?**
- Verify your API key is valid at [Google AI Studio](https://aistudio.google.com/app/apikey)
- Check if you have remaining quota/credits

**Q: Getting "Model experiencing high demand" error?**
- This is temporary - wait 5-10 minutes
- Try with a shorter resume
- Try during off-peak times

**Q: Results showing raw JSON instead of formatted?**
- Refresh the page (Ctrl+Shift+R)
- Clear browser cache
- Try with a shorter resume

**Q: Copy to Clipboard not working?**
- Only works over HTTPS or localhost
- Try manually selecting and copying text

## Features Coming Soon

- 📄 PDF export of analysis report
- 🎨 Multiple resume templates
- 🔄 Resume version history
- 📊 Analytics dashboard
- 🌙 Dark mode

## Contributing

Have ideas to improve the analyzer? 
- Fork the repository
- Create a feature branch
- Submit a pull request

## License

This project is open source and available under the MIT License.

## Author

**Jyothsna Peruri**
- GitHub: [@jyothsnaPeruri](https://github.com/jyothsnaPeruri)
- Project: [AI Resume Analyzer](https://github.com/jyothsnaPeruri/ai-resume-analyzer)

## Support

If you encounter any issues:
1. Check the [Troubleshooting](#troubleshooting) section
2. Visit [Google AI Studio](https://aistudio.google.com) for API issues
3. Check browser console (F12) for error messages

## Disclaimer

This tool is designed to provide suggestions and insights. Final resume and cover letter decisions should be made by the user. Always personalize and proofread before submission.

---

**Happy analyzing! 🚀**

Get your resume AI-powered today and land your dream job!
