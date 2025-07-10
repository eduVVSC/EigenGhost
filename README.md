# EigenGhost 👻

**EigenGhost** was the first monthly project at ISEP, where our goal was to emulate image operations using eigenvectors. The key tasks involved:

- Decomposing images;
- Reconstructing an image database;
- Searching for the closest image match;
- Generating a random image based on the database.

EigenGhost uses linear algebra techniques to perform these operations.  
> **Note:** The higher the number of eigenvalues (also known as "own values") used, the higher the fidelity of the resulting image.

---

## 🔧 Features

### 1. **Decompose**  
**Parameters:** `number of eigenvalues`, `image file (.csv)`  
Decomposes the input image using eigenvalue decomposition:

> **A = P D Pᵀ**  
> - **P**: matrix of eigenvectors  
> - **D**: diagonal matrix of eigenvalues  
> - **Pᵀ**: transpose of matrix P

Returns the decomposition data.  
> ⚠️ Currently for inspection only — not used directly elsewhere.

---

### 2. **Reconstruct Database**  
**Parameters:** `number of eigenvalues`, `directory of .csv images (database)`  
Fully reconstructs all images in the provided database using the selected number of eigenvalues.

---

### 3. **Search Closest Image**  
**Parameters:** `number of eigenvalues`, `database directory (.csv)`, `target image (.csv)`  
Searches the database for the image most similar to the input image using vector-space comparisons.

---

### 4. **Generate Random Image**  
**Parameters:** `number of eigenvalues`, `database directory (.csv)`  
Generates a new image based on the average of all images in the database, using random variation in the eigenvector space.

---

## 📦 Installation

Make sure to include the [Apache Commons Math 3.6.1](https://mvnrepository.com/artifact/org.apache.commons/commons-math3/3.6.1) library in your project dependencies.

---

## 🚀 Usage

### Interactive Mode
Run the application in interactive mode:
```bash
java -jar EigenGhosts.jar
## Usage

Running the code in an interactive mode (Not using arguments)
```java
java -jar EigenGhosts.jar
```

Running the code in an non interactive approach (Using arguments)
```java
java -jar EigenGhosts.jar -h #!! ASK FOR HELP !!
```
> You will get a full tutorial on how to use it. However you might take note of the following

-f X -k Y -i Z -d W

X -> Functionality number

Y -> Quantity of own values

Z -> Image path (.csv)

W -> Directory path [Also refered as database]

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Colaborators
[Tiago Lima](https://github.com/Tiago-Lima-TSL) - Dev

[Bernardo Correia](https://github.com/BKTales) - Dev

[Rodrigo Junqueira](https://github.com/junkeira13) - Dev

[Eduardo Vasconcelos](https://github.com/eduVVSC) - Scrum master

## License

[MIT](https://choosealicense.com/licenses/mit/)



