# Build a Full Stack App with Rust, Yew.rs and Actix Web

Note from Akhil - 
1. Before you do this project, make sure you Please watch the video preceeding this on from my youtube playlist first - https://youtube.com/playlist?list=PL5dTjWUk_cPYuhHm9_QImW7_u4lr5d6zO&si=PijWdMxQwWFUE7H0
2. Please watch the videos on actix, postgres (coming soon on my channel) and yew (coming soon) before you watch the video for this project and build it with me. This project is a bit on the difficult side.

In this project, I'll walk you through the process of building a backend API using the Actix web framework, SQLX, PostgreSQL, and Docker. Once we've created a powerful backend, we'll move on to building a single-page app using the Yew.rs framework. By the end of this tutorial, you'll have a fully functional web app that seamlessly integrates the frontend app with the backend API.

## Topics Covered

- Run the Full-Stack Rust App Locally
- Setup the Full-Stack Rust App
- Work on the Library Project
- Work on the Backend Project
    - Setup the Rust API Project
    - Setup PostgreSQL and pgAdmin with Docker
    - Database Migration with SQLX
    - Create the SQLX Database Model
    - Create the Request Validation Structs
    - Create the CRUD API Route Handlers
    - Register the API Routes and Setup CORS
- Work on the Frontend Project
    - Setup the Yew.rs Project
    - Setup Tailwind CSS for Styling
    - Create the API Request Functions
    - State Management with Yewdux
    - Create Reusable Components
    - Yew Component to Add New Feedback Item
    - Yew Component to Display Feedback Statistics
    - Yew Component to Display Feedback Information
    - Yew Component to Display the Feedback Items
    - Export the Component Files as Modules
    - Add the Components to the Main File
- Test the Rust Full-Stack App

## Instructions for setting up
- cd into the backend folder and run `docker-compose up -d`
- make sure you have rust installed and you're atleast on rustc 1.74 
- install `sqlx` with `cargo install sqlx-cli`, we will use this to run migrations
- once you're sure the docker containers for pg and pg-admin are running, run the migrations
with `sqlx migrate run`, you need to be in the backend folder to run this since the migrations folder is there
- then run `cargo run`, make sure you're in the backend folder
- to run the frontend which is in yew, we need trunk
- first install webassembly target - `rustup target add wasm32-unknown-unknown`
- then run `cargo install --locked trunk`
- then cd into the front end folder and run `trunk serve --port 3000`
- now, port 3000 is a common port and it's possible that some other process is already running there from before, so make sure you check and close that process
- finally, head over to `http://localhost:3000` to check the front end
- please note that if you don't run the front end on port 3000 and run it on another port, you will get 400 error when you try calling the APIs. 