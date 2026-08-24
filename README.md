# Front_End_Capstone

A responsive personal portfolio for Omolere Mojisola F., built with semantic
HTML, CSS, and lightweight JavaScript patterns. The site presents front-end
engineering, data control, and AI-assisted workflow case studies.

## Overview

The portfolio is the root-level site and includes a home page, an about page,
and a case-studies page. The repository also retains the earlier form
validation exercise in `files/` as a tested supporting demo.

## Features

- **Portfolio sitemap** – Home, About, and Case Studies pages with shared navigation
- **Responsive interface** – Mobile-first layouts built with CSS Grid and Flexbox
- **Case-study presentation** – Work covering front-end engineering, data control, and AfriFit
- **Accessible foundations** – Semantic HTML, descriptive image text, and keyboard-friendly links
- **Legacy validation demo** – A separated, tested contact-form validation exercise in `files/`

## Tech Stack

- **Frontend:** HTML5, CSS3, JavaScript
- **AI Integration:** Claude API
- **Tools:** Node.js, npm

## Prerequisites

- **Node.js (LTS)** - Download from [nodejs.org](https://nodejs.org)
- **Git** - Download from [git-scm.com](https://git-scm.com)
- **VS Code** (recommended) - Download from [code.visualstudio.com](https://code.visualstudio.com)

## Getting Started

```bash
# Clone the repository
git clone https://github.com/Mkof37/Front_End_Capstone.git

# Navigate to project
cd Front_End_Capstone

# Install dependencies
npm install

# Open the portfolio
# Use VS Code Live Server on index.html, or serve the repository root with any static server

# Start the legacy validation demo
npm start
```

## Scripts

- `npm start`: Serve the legacy `files/` demo with Live Server
- `npm run dev`: Serve the legacy demo on port 3000
- `npm test`: Run the legacy form-validation tests
- `npm run lint`: Run ESLint on JavaScript files in `files/`
- `npm run format`: Format the legacy demo files in `files/`

## Running Tests

Validation tests for the legacy demo are located in `files/test-validation.js`.
To execute them locally:

```bash
npm test
```

The tests verify:

- Empty field rejection
- Invalid email format detection
- Message length constraints
- Whitespace-only input handling
- Keyboard navigation and focus management

Ensure you have a recent Node.js LTS installed before running the scripts.

## Legacy Form Demo

### Contact Form

- **Name:** Required, non-whitespace input
- **Email:** Required, valid email format (requires @, domain, and TLD)
- **Message:** Required, minimum 10 characters

Validation occurs on form submit. All errors are announced to screen readers
via `aria-live` regions and displayed inline without blocking user workflow.
Invalid fields are marked with `aria-invalid="true"`.

## Project Structure

```text
Front_End_Capstone/
├── index.html                 # Portfolio home page
├── about.html                 # Portfolio biography and contact links
├── project.html               # Portfolio case studies
├── style.css                  # Shared portfolio styles
├── img/                       # Portfolio image assets
├── files/
│   ├── index.html             # Legacy validation demo
│   ├── app.js                 # Demo event handlers
│   ├── main.css               # Demo styles
│   ├── test-validation.js     # Demo test suite
│   ├── CLAUDE.md              # Local development guidelines copy
│   ├── WORKFLOW.md            # Vague vs. precise prompting case study
│   └── mnt/                   # Archive of previous iterations
├── .eslintrc.json             # ESLint configuration
├── .gitignore                 # Git ignore rules
├── package.json               # Project dependencies and scripts
├── package-lock.json          # Locked dependency versions
├── README.md                  # Project documentation
├── CLAUDE.md                  # Development guidelines and conventions
├── LICENSE                    # MIT License
└── node_modules/              # Installed dependencies (ignored in git)
```

## Development Approach

This capstone emphasizes precise prompting, accessible interfaces, and
testable implementation. Read [WORKFLOW.md](./files/WORKFLOW.md) for the
prompting case study and [CLAUDE.md](./CLAUDE.md) for repository conventions.

The root portfolio is static and can be previewed with the Live Server VS Code
extension. The npm scripts currently target the legacy demo in `files/`.

## License

MIT - See [LICENSE](./LICENSE) file for details

## Legacy Contact Form Example

The contact form demonstrates the project's core principles:

```html
<!-- Semantic HTML with labels and error regions -->
<form id="contact-form" class="contact-form">
  <fieldset>
    <legend>Send us a message</legend>
    
    <div class="contact-form__field">
      <label for="name">Name</label>
      <input 
        id="name" 
        type="text" 
        name="name" 
        required 
        aria-invalid="false"
        aria-describedby="name-error"
      />
      <div id="name-error" role="alert" class="contact-form__error"></div>
    </div>
    
    <div class="contact-form__field">
      <label for="email">Email</label>
      <input 
        id="email" 
        type="email" 
        name="email" 
        required 
        aria-invalid="false"
        aria-describedby="email-error"
      />
      <div id="email-error" role="alert" class="contact-form__error"></div>
    </div>
    
    <div class="contact-form__field">
      <label for="message">Message</label>
      <textarea 
        id="message" 
        name="message" 
        required 
        aria-invalid="false"
        aria-describedby="message-error"
      ></textarea>
      <div id="message-error" role="alert" class="contact-form__error"></div>
    </div>
  </fieldset>
  
  <button type="submit">Send Message</button>
</form>
```

Validation logic is defined in `files/test-validation.js` as pure functions and
can be imported and tested independently of the DOM via Node.js.

## Quality Standards Checklist

- [x] Code passes ESLint validation
- [x] Code is formatted with Prettier
- [x] All commits follow Conventional Commits format
- [x] README is clear and comprehensive
- [x] Project includes example/demo (Contact form)
- [x] Code includes comments for complex logic
- [x] Validation tests pass (`npm test`)
- [x] Forms use separated validation modules (no inline handlers)
- [x] All form inputs have associated labels
- [x] Error regions use `role="alert"` and `aria-invalid`

## Contributing

1. Follow [Conventional Commits](https://www.conventionalcommits.org/) format
2. Create feature branches from `main`
3. Write tests for new features and run `npm test` before committing
4. Submit pull requests with clear descriptions
5. Ensure ESLint passes: `npm run lint`
6. Format code: `npm run format`

---

**Status:** Portfolio sitemap and page layouts complete

**Last updated:** 2026-08-24
