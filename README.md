### 1. create github repository and make url (setting -> pages -> none to main -> save)

### 2. copy the url and paste it in package.json like below

```
{
  "name": "frontend-test-githubdeploy",
  "version": "0.1.0",
  "private": true,
  "homepage": "https://ramasamyfullstack.github.io/frontend-react-testdeploy",
  "dependencies": {
    "@testing-library/dom": "^10.4.1",
    "@testing-library/jest-dom": "^6.8.0",
    "@testing-library/react": "^16.3.0",
    "@testing-library/user-event": "^13.5.0",
    "react": "^19.1.1",
    "react-dom": "^19.1.1",
    "react-router-dom": "^7.9.1",
    "react-scripts": "5.0.1",
    "web-vitals": "^2.1.4"
  },
```
### 3. in BrouserRouter give basename="/repository-name" like below

```
import logo from './logo.svg';
import './App.css';
import { BrowserRouter, Link, Route, Routes } from 'react-router-dom';
import Read from './Read';
import Update from './Update';

function App() {
  return (
    <div className="App">
      <BrowserRouter basename='/frontend-react-testdeploy'>

        <Link to='/'>read</Link> <br />  <br />
        <Link to='/update'>update</Link>  <br />  <br />

      <Routes>
        <Route path='/' element={<Read />} />
        <Route path='/update' element={<Update />} />
      </Routes>
      
      </BrowserRouter>
    </div>
  );
}

export default App;

```

### 4. npm i -D gh-pages

### 5. npm run build

### 6. upload all the files from build folder into github repository

### 7. check the url
