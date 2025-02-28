
# React Documentation ⚛️

## 🚀 How to Start a New Project
To create a new React app, use:

```sh
npx create-react-app my-app
cd my-app
npm start
```
This starts a development server at `http://localhost:3000`.

---

## 🏗️ Creating a React Component
Create a new component `MyComponent.js`:

```jsx
import React from 'react';

const MyComponent = () => {
    return <h1>Hello, React! 🚀</h1>;
};

export default MyComponent;
```

Use it in `App.js`:

```jsx
import MyComponent from './MyComponent';

function App() {
    return (
        <div>
            <MyComponent />
        </div>
    );
}

export default App;
```

---

## 🎨 Best UI Libraries
Choosing the right UI library improves development efficiency.

### 1️⃣ **Material-UI (MUI)**
- Install:
  ```sh
  npm install @mui/material @emotion/react @emotion/styled
  ```
- Usage:
  ```jsx
  import { Button } from '@mui/material';

  function App() {
      return <Button variant="contained">Click Me</Button>;
  }
  ```

### 2️⃣ **Skeleton.dev**
- Minimalist UI framework for lightweight components.
- Install:
  ```sh
  npm install @skeletonlabs/skeleton
  ```
- Usage:
  ```jsx
  import { Button } from '@skeletonlabs/skeleton';

  function App() {
      return <Button>Click Me</Button>;
  }
  ```

Both are great choices depending on your project needs! 🏆

