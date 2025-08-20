# Evolutionary Sandbox

This project is an interactive web application that allows users to simulate and visualize evolutionary concepts. It features a dynamic predator-prey simulation and a powerful node-based visual programming editor to control creature traits. The application leverages AI to analyze simulation data and provide insightful summaries.

## Key Features

- **Dynamic Visual Simulation**: Watch creatures (prey) and predators interact in a 2D environment. Creatures must eat from bushes to maintain energy, while predators hunt creatures to survive.
- **Parameter Controls**: Adjust creature traits like mutation rate, speed, and size. Modify environmental factors such as temperature, water level, and sunlight to see how they impact the ecosystem.
- **Visual Programming Editor**:
    - A full-featured, node-based editor to define creature logic visually.
    - Drag and drop various node types from a sidebar onto the canvas.
    - Connect nodes to build complex behaviors and apply them directly to the simulation.
- **AI-Powered Analysis**: Run the simulation and get an AI-generated statistical analysis, complete with charts, that summarizes evolutionary trends in population size, genetic drift, and trait changes.
- **Dual View**: Seamlessly switch between the main simulation dashboard and the visual programming editor.

## Tech Stack

- **Framework**: [Next.js](https://nextjs.org/) (with App Router)
- **Language**: [TypeScript](https://www.typescriptlang.org/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **UI Components**: [ShadCN UI](https://ui.shadcn.com/)
- **Visual Editor**: [React Flow](https://reactflow.dev/) (`@xyflow/react`)
- **Generative AI**: [Firebase Genkit](https://firebase.google.com/docs/genkit)

## Getting Started

Follow these instructions to get a local copy up and running.

### Prerequisites

You need to have [Node.js](https://nodejs.org/en/) (version 20 or later) and npm installed on your machine.

### Installation & Running the App

1.  **Clone the repository:**
    ```bash
    git clone <https://github.com/spacenachos/evolution-simulation-template>
    cd <repository-folder>
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Set up environment variables:**
    Create a `.env` file in the root of the project. If you plan to use the AI analysis features, you will need to add your Google AI API key.
    ```
    GEMINI_API_KEY=your_api_key_here
    ```

4.  **Run the development server:**
    The application requires two development servers to run concurrently: one for the Next.js frontend and one for the Genkit AI flows.

    - **In your first terminal, run the Next.js app:**
      ```bash
      npm run dev
      ```
      This will start the main application on [http://localhost:9002](http://localhost:9002).

    - **In a second terminal, run the Genkit watcher:**
      ```bash
      npm run genkit:watch
      ```
      This starts the local Genkit server that the Next.js app communicates with for AI features.

5.  **Open the application:**
    Open [http://localhost:9002](http://localhost:9002) in your browser to see the application.
