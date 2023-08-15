# React Router
- **Install React Router Dom**
  
```javascript
  npm i react-router-dom
```

- **Create route.js file inside src/router and copy this code and past it inside route.js** 

```javascript
import { Route, Routes } from "react-router-dom";
import MainLayout from "../layout/MainLayout";

// Page
import Home from "../pages/Home";
import Story from "../pages/Story";
import StoryDetails from "../pages/StoryDetails";

export default function router() {
  return (
    <Routes>
      <Route path="/" element={<MainLayout />}>
        <Route index element={<Home />} />
        <Route path="stories" element={<Story />} />
        <Route path="stories/:slug" element={<StoryDetails />} />
      </Route>
    </Routes>
  );
}

```


- **Copy this code inside MainLayout.jsx**
```javascript 
import Header from './Header'
import Footer from './Footer'
import { Outlet } from 'react-router'

function MainLayout() {
  return (
      <>
          <Header />
          <Outlet/>
          <Footer/>
      </>
  )
}

export default MainLayout
```

- **Copy this code inside App.jsx**
```javascript 
import { BrowserRouter } from "react-router-dom";
import CustomRouter from "./route/router";

function App() {
  return (
    <>
      <BrowserRouter>
        <CustomRouter />
      </BrowserRouter>
    </>
  );
}

export default App;

```
