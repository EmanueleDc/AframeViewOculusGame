# AframeViewOculusGame
A-Frame Game Viewer

# VR Target Throw – A-Frame + MQTT Web Viewer

A web-based real-time viewer for a VR target throwing game, built with **A-Frame** and **Paho MQTT**.

This project provides a browser-based visualization of a game where players, using a VR headset, throw a ball at a target to score points. Game events and state are synchronized in real time through **MQTT over WebSockets**, using **JSON** messages for communication.

The application acts as a live spectator and monitoring interface, receiving the same game data exchanged with:

* A **Unity mobile application**.
* A **Unity application for Meta Quest / Oculus**.
* This **A-Frame web client**, which renders the game state directly in the browser.

## Features

* 🎯 Real-time visualization of the target throwing game.
* 🥽 Designed to work alongside VR gameplay.
* 🌐 Browser-based 3D scene powered by **A-Frame**.
* 📡 Real-time communication using **Paho MQTT** over **WebSockets**.
* 📦 JSON-based messaging protocol shared across all clients.
* 🏆 Live score tracking and game state updates.
* 🔄 Cross-platform synchronization between Web, Unity Mobile, and Meta Quest/Oculus applications.

## Technologies

* A-Frame
* Paho MQTT JavaScript Client
* MQTT over WebSockets
* JSON
* HTML / JavaScript

## Architecture

The system follows a publish/subscribe architecture:

* The VR game publishes gameplay events (ball throws, score updates, game state) as JSON messages via MQTT.
* Unity applications and the A-Frame web viewer subscribe to the same topics.
* Every connected client stays synchronized in real time, providing a consistent view of the match regardless of the platform.

## Use Cases

* Live spectator view from any web browser.
* Real-time score monitoring.
* Multi-device synchronization.
* Debugging and development of the VR game.
* Demonstration of MQTT-based communication between Unity and WebXR applications.
