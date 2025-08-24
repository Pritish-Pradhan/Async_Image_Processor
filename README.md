Asynchronous Image Processor with Parallel Rendering (JavaFX)

📖 Overview

A Java-based image processing engine that applies filters (e.g., grayscale) on images asynchronously by splitting them into smaller tiles and processing them in parallel. Results are rendered dynamically on a JavaFX Canvas in real time.

🚀 Features

Asynchronous processing using Java’s ExecutorService with thread pooling.

Tile-based image segmentation for parallel filter application.

Real-time rendering with JavaFX and a queue-based draw system.

Extensible filter design (ImageFilter interface) to easily add new filters.

Non-blocking UI updates using Platform.runLater() and AnimationTimer.

🖼️ Demo

(Add a before/after image or a short GIF showing grayscale transformation in progress)

⚙️ Tech Stack

Language: Java

UI: JavaFX (Canvas, Scene, AnimationTimer)

Concurrency: ExecutorService, Callable, Future

Image I/O: javax.imageio

📂 Project Structure
com.image.imageprocessing
 ├── filter
 │    ├── ImageFilter.java
 │    └── GreyScaleFilter.java
 ├── image
 │    ├── DrawMultipleImagesOnCanvas.java
 │    └── ImageData.java
 ├── io
 │    ├── FileImageIO.java
 │    └── ImageReadInf.java
 ├── processor
 │    └── ImageProcessor.java
 └── HelloApplication.java

🛠️ How to Run

Clone the repo

Add your test image path in HelloApplication.java

Run the project with JavaFX enabled

mvn clean install
java --module-path "path/to/javafx-sdk/lib" --add-modules javafx.controls,javafx.fxml -jar target/app.jar
