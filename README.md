# Artemis UI

Artemis UI Component Library is a comprehensive collection of UI components, designed for the Artemis education platform. Leveraging Storybook, it offers an interactive and user-friendly environment for both the development and showcasing of UI components. The library's primary aim is to incorporate all UI components utilized on [Artemis](https://artemis.ase.in.tum.de), ensuring a cohesive and efficient design system.


## Getting Started

### Prerequisites
Ensure you have the latest version of Node.js and npm installed on your system, as they are necessary for building and managing Angular projects. You can download and install Node.js from [nodejs.org](https://nodejs.org/en).


### Installation
1. **Clone the Repository:** Open your terminal and execute the following command to clone the repository:
```bash
git clone https://github.com/bgeisb/artemis-ui.git
```

2. **Navigate to the Project Directory:**
After cloning, switch to the project directory:
```bash
cd artemis-ui
```

3. **Install Dependencies:**
Run the following command to install all necessary dependencies:
```bash
npm install
```

### Starting Storybook
To preview the UI components in Storybook, execute the following command: 
```bash
npm run storybook
```
This will start the Storybook server, and you can view the components in your browser at the provided URL (usually http://localhost:6006).

### Integrating Artemis UI into Your Project
To use the components in your Angular project, import the desired component modules into your app module or the specific module where you want to use them.
```node
import { ExampleComponent } from 'artemis-ui';

@NgModule({
  declarations: [
    // ...
    ExampleComponent
  ],
  // ...
})
export class YourModule { }
```

## Adding New Components
If you're looking to expand the Artemis UI Component Library by adding new components, follow these steps to ensure a smooth integration into our existing structure and Storybook.

### Step 1: Generating the Component
1. **Navigate to the Components Directory:** Make sure you're in the correct directory where existing components are housed:
```bash
cd ./projects/design-system/src/lib
```

2. **Generate the New Component:** 
Use Angular CLI to generate a new component. Replace `<component-name>` with the name of your component:
```bash
ng generate component <component-name>
```
This command creates a new folder within the lib directory, including all necessary files for defining your component (like TypeScript, HTML, and CSS files).

### Step 2: Setting Up Storybook Integration
After generating the component, you'll need to manually set up its integration with Storybook:

1. **Create a Storybook File:**
In the newly created component folder, add a Storybook file named `<component-name>.stories.ts`. This is where you'll define the story for your component, enabling it to be previewed in Storybook.

2. **Define Your Story:**
Inside the `.stories.ts` file, write the necessary code to tell Storybook how to render and interact with your component. This typically involves importing the component and defining a default export and a story that represents your component in different states.

For further information on Stories go check out Storybook's documentation on [how to write stories](https://storybook.js.org/docs/react/writing-stories/introduction).


## Additional Resources

### Artemis
- [Production System](artemis.ase.in.tum.de)
- [Documentation](docs.artemis.cit.tum.de)
- [Repository](https://github.com/ls1intum/Artemis)

### Angular
To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page

### Storybook
- [Write Stories](https://storybook.js.org/docs/react/writing-stories/introduction)
- [Write Docs](https://storybook.js.org/docs/react/writing-docs/introduction)
- [Testing](https://storybook.js.org/docs/react/writing-tests/introduction)
- [Storybook in Figma](https://storybook.js.org/docs/react/sharing/design-integrations)
