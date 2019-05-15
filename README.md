# AWS Amplify React Native Events App (Workshop)

Workshop project demonstrating a React Native (Expo) mobile app backed by AWS Amplify and AWS AppSync (GraphQL), with optional analytics (Amazon Pinpoint) and a CI/CD extension lab.

This repository is structured as a set of hands-on labs. The runnable mobile app source lives under `sample/`.

## Repository layout

- `sample/`: React Native (Expo) application source code
- `setup/`: Cloud9 + Docker + Expo setup instructions (workshop environment)
- `amplify/`: Amplify CLI workflow (init/auth/functions, etc.)
- `appsync/`: AppSync (GraphQL API) lab content
- `pinpoint/`: Analytics lab content
- `cicd/`: Optional CI/CD lab content (CodeBuild/CodePipeline/Device Farm)
- `reactnative-docker/`: Docker environment notes

## Quick start (local machine)

> The original workshop uses AWS Cloud9 + Docker. If you’re running locally, you can typically run the app directly with Node/Yarn and the Expo CLI.

### Prerequisites

- Node.js (LTS recommended)
- Yarn
- Expo CLI (or use `npx expo ...`)
- AWS account + AWS CLI credentials (for Amplify/AppSync provisioning)
- AWS Amplify CLI (`@aws-amplify/cli`)

### Install and run

```bash
cd sample
yarn
yarn start
```

Then open the app in Expo Go (or an emulator) following the Expo instructions printed in the terminal.

## Backend setup (Amplify + AppSync)

The backend is provisioned via the Amplify CLI. Follow the lab docs in order:

- `setup/README.md` (only required if using Cloud9 + Docker)
- `amplify/README.md`
- `appsync/README.md`
- `pinpoint/README.md` (optional)

## Security notes

- Do not commit credentials, secrets, or generated backend outputs containing account-specific identifiers.
- If you create local env files (for example `.env`), keep them untracked and add them to `.gitignore`.

## Troubleshooting

- **Expo can’t reach packager**: ensure your device and dev machine/network can reach the Expo dev server; if using Cloud9, inbound ports must allow `19000-19001`.
- **Amplify “credentials not found”**: ensure your AWS profile/credentials are configured and have sufficient permissions for the workshop.

## License

See the repository license file (if present) and third-party dependency licenses under `sample/ios/Pods` as applicable.

