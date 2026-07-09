# Photo Search System for Running Events

A microservice-based API application designed to help participants of amateur running events find their photos automatically.

The system processes race participant data, GPS tracks (`.gpx` files), and photo metadata to calculate the probability that a specific participant appears in a given photo. The service provides an API endpoint for searching and returns a ranked list of photos with corresponding confidence scores and file locations.

## Architecture

* **Backend:** Node.js + Express
* **API:** REST API for photo search requests
* **Algorithm module:** C++ implementation integrated with Node.js using N-API
* **Data processing:** Photo metadata analysis and participant GPS track matching

## How it works

1. A user sends a search request with participant information and race data.
2. The server processes available event photos and participant track data.
3. The C++ algorithm module calculates the probability of a participant appearing in each photo.
4. The API returns matching photos with confidence scores.

## Technologies

* JavaScript / Node.js
* Express.js
* C++
* Node.js N-API
* REST API
* GPS track processing (GPX)
* Microservice architecture

## Project Structure

* `myserver.js` — Node.js server implementation
* `algorithm/` — C++ algorithm module
* `pod.cpp / pod.h` — probability calculation logic
* `napipod.cpp / napipod.h / main.cpp` — Node.js native addon integration
* `binding.gyp` — N-API build configuration

## Documentation

- [Project presentation](docs/Photo_Search_System_Architecture_and_Algorithm.pptx)

The presentation provides an overview of the system architecture, algorithm approach, and implementation details.

The project demonstrates integration between a web API service and a high-performance native C++ module for computational tasks.
