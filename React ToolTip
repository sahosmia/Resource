TootlTip


Create Tooltip Component inside components/core and copy this code and past it inside Tooltip Component 

```javascript
import React, { useState } from "react";
import PropTypes from "prop-types";

const Tooltip = ({ content, children }) => {
  const [isTooltipVisible, setTooltipVisible] = useState(false);

  const handleMouseEnter = () => {
    setTooltipVisible(true);
  };

  const handleMouseLeave = () => {
    setTooltipVisible(false);
  };

  return (
    <div className="relative inline">
      <div
        className="inline-block"
        onMouseEnter={handleMouseEnter}
        onMouseLeave={handleMouseLeave}
      >
        {children}
      </div>
      {isTooltipVisible && (
        <div className="text-xs font-thin rounded text-white absolute whitespace-nowrap  top-full left-1/2 -translate-x-1/2 p-1 bg-neutral-900">
          {content}
        </div>
      )}
    </div>
  );
};

Tooltip.propTypes = {
  content: PropTypes.node.isRequired,
  children: PropTypes.node.isRequired,
};
export default Tooltip;


```


Copy this code and past it inside App.jsx
```javascript 
import { useState } from "react";
import "./App.css";
import { BiAperture } from "react-icons/bi";
import Tooltip from "./components/core/Tooltip";

function App() {
  const [count, setCount] = useState(0);

  return (
    <>
      <div>
        <h2 className="text-red-400" title="Setting">
          <BiAperture />
        </h2>

        <div className="tooltip-trigger">
          Tooltip Trigger
          <div className="tooltip tooltip-right">Tooltip Text</div>
        </div>

        <Tooltip content="This is a tooltip!">
          <button>Hover Me</button>
        </Tooltip>
      </div>
    </>
  );
}

export default App;
```
