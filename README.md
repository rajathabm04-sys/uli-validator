# 🔐 ULI Security Document Validator

**IP/URL Whitelisting - L1 Validation Tool**

A browser-based validation tool for ULI Platform security documents, ensuring compliance with IFTAS requirements before submission.

[![Live Demo](https://img.shields.io/badge/Live-Demo-success)](https://YOUR_USERNAME.github.io/uli-validator/)
[![Version](https://img.shields.io/badge/version-1.0-blue)]()
[![License](https://img.shields.io/badge/license-MIT-green)]()

---

## 📋 Overview

This tool validates **ALL 3 MANDATORY** security documents required for ULI Platform IP/URL whitelisting:

- 🛡️ **Anti-Malware Solution** - Validates deployment documentation
- 📐 **Architecture Diagram** - Validates system integration documentation  
- 🔍 **VAPT Report** - Validates CERT-IN empaneled audit reports

### Key Features

✅ **Comprehensive Validation** - 20+ validation checks across 3 document types  
✅ **OCR Support** - Automatically processes scanned PDFs  
✅ **100% Private** - All processing happens in your browser, no data uploaded  
✅ **Instant Feedback** - Know immediately if documents will pass IFTAS review  
✅ **Professional UI** - Clean, intuitive interface with step-by-step guidance

---

## 🚀 Quick Start

### **Option 1: Use Online (Recommended)**

Visit the live tool: **[https://YOUR_USERNAME.github.io/uli-validator/](https://YOUR_USERNAME.github.io/uli-validator/)**

### **Option 2: Run Locally**

1. Clone this repository:
```bash
git clone https://github.com/YOUR_USERNAME/uli-validator.git
cd uli-validator
```

2. Open `index.html` in your browser:
```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html
```

---

## 📖 How to Use

### Step 1: Select Document Type
Choose which document you want to validate:
- Anti-Malware Solution
- Architecture Diagram
- VAPT Report

### Step 2: Upload Document
- Supported formats: PDF, DOCX, TXT
- Works with both text-based and scanned PDFs (OCR enabled)
- File size limit: Recommended < 10MB

### Step 3: Validate
Click "VALIDATE DOCUMENT" and review results:
- ✅ Green checkmarks = Passed requirements
- ❌ Red X marks = Failed requirements (needs fixing)
- ⚠️ Yellow warnings = Recommended improvements

### Step 4: Fix & Revalidate
Address any failures and upload again until all checks pass.

---

## 📝 Validation Criteria

### 🛡️ Anti-Malware Solution (6 Checks)

**Critical:**
- Anti-malware solution documented
- Anti-ransomware controls present
- Implementation details/writeup
- Source module coverage

**Recommended:**
- Screenshots/evidence provided
- Cloud justification (if hosted on cloud)

### 📐 Architecture Diagram (7 Checks)

**Critical:**
- Diagram/visual representation present
- ULI platform integration highlighted
- Key systems documented (CBS/LOS/LMS)
- Data flow documentation
- API interactions documented
- Communication/integration explained

**Recommended:**
- Detailed writeup/explanation

### 🔍 VAPT Report (7 Checks)

**All Critical:**
- CERT-IN empaneled auditor
- Report within 6 months
- Both VA and PT conducted
- Risk summary table present
- No LOW findings with HIGH impact
- All vulnerabilities closed
- Technical details match source module

---

## 🔒 Privacy & Security

### Your Data is Safe

- ✅ **100% Client-Side Processing** - Everything runs in your browser
- ✅ **No Server Uploads** - Documents never leave your computer
- ✅ **No Data Storage** - Nothing is saved or logged
- ✅ **No Analytics** - No tracking, cookies, or monitoring
- ✅ **Offline Capable** - Works without internet after first load

### Technology Stack

- **PDF Processing**: PDF.js (Mozilla)
- **OCR**: Tesseract.js
- **Document Parsing**: docx.js, mammoth.js
- **UI**: Vanilla JavaScript (no frameworks)

---

## 📊 Supported Document Formats

| Format | Support | OCR | Notes |
|--------|---------|-----|-------|
| PDF (text-based) | ✅ | N/A | Fast processing |
| PDF (scanned) | ✅ | ✅ | 10-30 sec/page |
| DOCX | ✅ | N/A | Microsoft Word |
| TXT | ✅ | N/A | Plain text |

---

## 🎯 For RBIH Team

### Pilot Program

This tool is currently in **pilot phase** for ULI Platform lender onboarding.

**Feedback Channels:**
- Report issues: Create GitHub issue
- Suggest improvements: Pull requests welcome
- Contact: support@uli.rbih.in

### Known Limitations

⚠️ **Current Limitations:**
- OCR accuracy: 90-95% (quality-dependent)
- Scanned PDF processing: Slower (10-30 sec/page)
- Large files (>20MB): May be slow
- Handwritten text: Limited support

### Roadmap

🔮 **Coming Soon:**
- Batch validation (multiple files)
- Export validation reports
- Custom validation rules

---

## 🛠️ Technical Details

### Browser Requirements

- **Chrome/Edge**: Recommended (v90+)
- **Firefox**: Supported (v88+)
- **Safari**: Supported (v14+)
- **Mobile**: iOS Safari, Chrome Android

### Performance

| Operation | Time | Notes |
|-----------|------|-------|
| Text PDF (10 pages) | < 2 sec | Fast |
| Scanned PDF (10 pages) | 2-5 min | OCR processing |
| DOCX | < 1 sec | Fast |
| Validation checks | < 1 sec | All document types |

---

## 📚 Documentation

### For Developers

The validation rules are defined in the `RULES` object:

```javascript
const RULES = {
    vapt: { /* 7 checks */ },
    antimalware: { /* 6 checks */ },
    architecture: { /* 7 checks */ }
};
```

Each check has:
- `name`: Check description
- `critical`: Boolean (must pass for approval)
- `validate`: Function returning `{pass, msg}`

### For End Users

Detailed documentation available at: [IFTAS Security Document Checklist](URL_TO_CHECKLIST)

---

## 🤝 Contributing

Contributions welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **RBIH Team** - Requirements and testing
- **IFTAS** - Security standards
- **Mozilla** - PDF.js library
- **Tesseract.js** - OCR capability

---

## 📞 Support

**For Technical Issues:**
- GitHub Issues: [Create an issue](https://github.com/YOUR_USERNAME/uli-validator/issues)

**For ULI Platform Questions:**
- Email: support@uli.rbih.in
- Subject: ULI Security Document Validator

---

## 🔄 Version History

### v1.0.0 (January 2026)
- ✅ Initial release
- ✅ 3 document types supported
- ✅ 20 validation checks
- ✅ OCR for scanned PDFs
- ✅ Centered UI with usage instructions
- ✅ Fixed LOW+HIGH impact detection

---

**Built with ❤️ for the ULI Platform**

**Last Updated:** January 2026
