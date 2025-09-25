# ReactDashboardAssessment

# Dashboard.jsx

import { useState } from "react";
import Counter from "./Counter";

// A simple presentational component for notes.
// In a larger application, this would be in its own file.
function Notes({ notes }) {
    return (
        <div>
            <h2>Notes</h2>
            <ul>
                {notes.map((note, index) => <li key={index}>{note}</li>)}
            </ul>
        </div>
    );
}

export default function Dashboard() {
    const [counter, setCounter] = useState(0);
    const notes = ['First note', 'Another note'];

    const handleIncrement = () => setCounter(currentCount => currentCount + 1);
    const handleDecrement = () => setCounter(currentCount => currentCount - 1);

    return (
        <>
            <h1>Dashboard</h1>
            <Counter count={counter} onIncrement={handleIncrement} onDecrement={handleDecrement} />
            <Notes notes={notes} />
        </>
    )
}


# Counter.jsx

export default function Counter({ count, onIncrement, onDecrement }) {
    return (
        <div style={{ margin: "10px 0" }}>
            <button onClick={onIncrement}>+</button>
            <span style={{ margin: "0 10px", fontSize: "1.5em" }}>
                {count}
            </span>
            <button onClick={onDecrement}>-</button>
        </div>
    );
}

# Notes.jsx
I didn't get this far
