# AnvitStore 🛍️

[![AWS Amplify](https://img.shields.io/badge/Deployed%20on-AWS%20Amplify-orange)](https://aws.amazon.com/amplify/)

A developer-focused e-commerce store selling programming-themed stickers and planners, built with Next.js and deployed with AWS Amplify for full-stack hosting.

🔗 **Live Store**: [https://master.d2j81piylpyl5g.amplifyapp.com](https://master.d2j81piylpyl5g.amplifyapp.com)

![AnvitStore Showcase](https://via.placeholder.com/1200x600?text=AnvitStore+AWS+Deployment) 

## Features 🚀
- 🛒 **Developer Merchandise**: Stickers featuring programming language logos
- 🔄 **Full-Stack Deployment**: Frontend + backend on AWS Amplify
- 💳 **Stripe Integration**: Secure payment processing
- 📦 **Order Management**: Backend API for order processing
- 📱 **Responsive Design**: Mobile-first approach

## Tech Stack 💻
### Frontend
- Next.js 14 (App Router)
- Tailwind CSS
- Stripe Checkout

### Backend
- Next.js API Routes
- AWS Amplify Hosting

## AWS Amplify Deployment 🌐

### Prerequisites
- AWS account
- Amplify CLI installed
- Stripe account

### Deployment Steps
1. **Initialize Amplify**:
```bash
npm install -g @aws-amplify/cli
amplify init
```

2. **Configure Backend:**:
```bash
amplify add api
# Select REST or GraphQL based on your needs
amplify add auth # For authentication
```

3. **Environment Variables:**:
```bash
STRIPE_SECRET_KEY=your_live_key
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=your_pk_key
NEXT_PUBLIC_AMPLIFY_ENDPOINT=your_api_endpointn
```

4. **Build Settings:**:
```bash
version: 1
frontend:
  phases:
    preBuild:
      commands:
        - npm ci
    build:
      commands:
        - npm run build
  artifacts:
    baseDirectory: .next
    files:
      - '**/*'
  cache:
    paths:
      - node_modules/**/*
```

5. **Deploy:**:
```bash
amplify push
amplify publish
```

## Troubleshooting 🛠️
Common Amplify issues:

- Build Fails: Check Node.js version in build settings

- API Timeouts: Increase Lambda timeout duration

- Env Vars Missing: Verify in Amplify Console > Environment variables

## Contributing 🤝
I welcome contributions! Please follow these steps:

- Fork the repository

- Create a new branch (git checkout -b feature/your-feature)

- Commit your changes (git commit -m 'Add some feature')

- Push to the branch (git push origin feature/your-feature)

- Open a Pull Request

Please ensure your code follows the existing style and includes appropriate tests.

## Support ❤️
If you find Spendorra useful, consider:

- ⭐ Starring this repository on GitHub

- 🐛 Reporting issues in the GitHub Issues section

- 💡 Suggesting new features
