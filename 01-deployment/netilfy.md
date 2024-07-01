# Deploying Vite React Project on Netlify

Netlify is a web hosting and automation platform which you can use to deploy your static sites. You will have to Sign up to Netlify if you don’t have an account already and then you can create a new app from their menu.

## Deployment Manually

### 1. Prepare Your Vite React Project

- **Generate Production Build:**
  Use the following command to generate a production build of your Vite React project:

  ```bash
  npm run build
  ```

  This command will create a `dist` directory containing optimized and minified assets.

### 2. Create a Netlify Account

- **Sign Up for Netlify:**
  If you don't have a Netlify account, sign up at [Netlify](https://www.netlify.com/).

### 3. Connect to GitHub

- **Connect GitHub Repository:**
  Connect your Vite React project repository to Netlify from the Netlify dashboard. This allows Netlify to automatically deploy your project whenever changes are pushed to the connected repository.

### 4. Configure Build Settings

- **Specify Build Command and Output Directory:**
  In the Netlify dashboard, go to "Site settings" -> "Build & deploy" -> "Build settings." Set the build command to:

  ```bash
  npm run build
  ```

  And set the output directory to:

  ```bash
  dist
  ```

  This ensures that Netlify uses your Vite production build for deployment.

### 5. Environment Variables

- **Set Environment Variables:**
  If your Vite React project requires environment variables, set them in the Netlify dashboard under "Site settings" -> "Build & deploy" -> "Environment."

### 6. Deploy

- **Trigger Manual Deployment:**
  Manually trigger the deployment in the Netlify dashboard or push a change to your connected GitHub repository to automatically trigger a deployment.

- **View Deployment Logs:**
  Monitor the deployment process in the Netlify dashboard under "Deploys." View logs to identify any issues during the deployment.

### 7. Testing

- **Test Your Deployed Application:**
  Once the deployment is successful, test your Vite React application on the provided Netlify URL. Ensure all features work as expected.

## Deploy using Netlify CLI

### 1. **Install Netlify CLI:**

Ensure you have the Netlify CLI installed globally on your machine. If not, install it using the following npm command:

```bash
npm install -g netlify-cli
```

### 2. **Build Your Vite React Project:**

Generate a production build for your Vite React project. Use the following command in your project directory:

```bash
npm run build
```

This command will create a `dist` directory containing the optimized production build.

### 3. **Navigate to the Build Output Directory:**

Go to the root directory of your Vite React project, and navigate to the `dist` directory:

```bash
cd dist
```

### 4. **Initialize a New Git Repository (If not already done):**

If your project is not a Git repository, initialize one:

```bash
git init
```

### 5. **Login to Netlify:**

Run the following command to log in to your Netlify account:

```bash
ntl login
```

Follow the prompts to authenticate and grant access to your Netlify account.

### 6. **Create a New Site on Netlify:**

Use the following command to create a new site on Netlify. This command will also link your local Git repository to the newly created Netlify site:

```bash
ntl init
```

Follow the prompts to set up the site. Choose the appropriate options, including the build command and directory.

### 7. **Deploy Your Site:**

Once the initialization is complete, deploy your site to Netlify:

```bash
ntl deploy
```

This command will prompt you to specify the directory to deploy. Enter the path to the `dist` directory.

### 8. **Configure Site Settings (Optional):**

You can configure site settings interactively or by modifying the `netlify.toml` file generated during the initialization. This includes specifying environment variables, redirects, and other settings.

### 9. **View Your Deployed Site:**

After the deployment is complete, Netlify will provide you with a unique URL where your Vite React project is hosted. Open this URL in a browser to view your deployed application.

### 10. **Testing:**

Thoroughly test your deployed Vite React application to ensure all features work as expected on the Netlify-hosted environment.
