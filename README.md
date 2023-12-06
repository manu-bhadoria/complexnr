## Introduction
`complexnr` is a library for handling complex numbers in Noir. This library offers a comprehensive suite of operations for complex numbers.

## Features
The library provides a variety of functions to manipulate complex numbers, ensuring high precision and efficiency, crucial for cryptographic applications:

- `add(a: Complex, b: Complex)`: Adds two complex numbers.
- `subtract(a: Complex, b: Complex)`: Subtracts one complex number from another.
- `multiply(a: Complex, b: Complex)`: Multiplies two complex numbers.
- `divide(a: Complex, b: Complex)`: Divides one complex number by another.
- `scalar_multiply(complex: Complex, scalar: Field)`: Multiplies a complex number by a scalar.
- `conjugate(complex: Complex)`: Computes the conjugate of a complex number.
- `squared_magnitude(complex: Complex)`: Calculates the squared magnitude of a complex number.
- `sqrt(value: Field, iterations: u32)`: Approximates the square root of a field value.
- `magnitude(complex: Complex, iterations: u32)`: Calculates the magnitude of a complex number.
- `evaluate_polynomial(coefficients: [Field; 10], x: Complex)`: Evaluates a polynomial at a given complex number.

## Importance for Zero-Knowledge Proofs
In the realm of ZKPs, the `complexnr` library plays a crucial role. Complex number calculations are essential in various cryptographic protocols and algorithms. This library ensures that these calculations are performed with the requisite precision and efficiency, which is paramount in maintaining the integrity and security of ZKPs.

## Installation
To use `complexnr` in your Noir project, include it in your `Nargo.toml` and import it in your Noir files.

## Usage
Below are examples of how to use the library:

```noir
// Create complex numbers
let a = Complex { real: 1, imaginary: 2 };
let b = Complex { real: 3, imaginary: 4 };

// Perform operations
let sum = add(a, b);
let difference = subtract(a, b);
```
## Limitations and Considerations
While `complexnr` is designed for high efficiency and precision, there are some inherent limitations and considerations to be aware of:

- **Precision**: Due to the nature of field arithmetic in ZKPs, there may be limitations in the precision of complex number operations, especially when dealing with very large numbers.
- **Computational Complexity**: Some complex number operations can be computationally intensive, which should be considered when designing algorithms for ZK environments.
- **Functionality Scope**: Currently, the library focuses on basic arithmetic operations. Advanced functions like trigonometric or logarithmic operations for complex numbers are not yet implemented.
- **Iterative Methods**: Functions like `sqrt` use iterative methods for approximation, which may not always yield the exact results, especially with a limited number of iterations.

## Testing

`complexnr` comes with a suite of tests ensuring the accuracy and reliability of its functions. Run these tests using Noir's testing framework to verify the functionality.

## Contribution

Contributions to `complexnr` are welcome! Whether it's extending functionality, improving efficiency, or enhancing documentation, your input is valuable.

## License

`complexnr` is released under Apache 2.0 License.
