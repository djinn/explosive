# Explosive: Heston Model of Volatility in Python

Explosive is a Python library for working with the Heston Model of Volatility in the field of quantitative finance. This library provides a set of tools and functions to simulate, calibrate, and analyze the Heston Model, a widely-used mathematical model for describing the dynamics of financial asset prices with stochastic volatility.

## Features

- **Simulation:** Generate paths of asset prices and corresponding volatilities based on the Heston Model.
- **Calibration:** Calibrate the model to market data, finding the optimal parameters to match observed option prices or implied volatilities.
- **Pricing:** Calculate option prices and Greeks (Delta, Gamma, Vega, Theta) using the Heston Model.
- **Analysis:** Analyze model outputs, including statistical metrics and risk measures.

## Getting Started

1. **Installation:**

   Install Explosive using pip:

   ```shell
   pip install explosive
   ```

2. **Usage:**

   Import the library and start using the Heston Model functions in your Python code:

   ```python
   from explosive import HestonModel

   # Create a HestonModel instance
   heston = HestonModel()

   # Simulate asset price and volatility paths
   paths = heston.simulate_paths(...)

   # Calibrate the model to market data
   calibrated_params = heston.calibrate(...)

   # Price options using the calibrated model
   option_price = heston.price_option(...)

   # Analyze model outputs and risk measures
   statistics = heston.analyze(...)
   ```

3. **Documentation:**

   For detailed documentation and examples, refer to the [Explosive Documentation](https://explosive-library.com/documentation).

4. **Contributing:**

   Contributions are welcome! If you'd like to contribute to the development of Explosive, please follow our [Contributing Guidelines](CONTRIBUTING.md).

5. **License:**

   Explosive is distributed under the MIT License. See the [LICENSE](LICENSE) file for more information.

## Example

```python
# Sample code for simulating Heston Model paths
from explosive import HestonModel

# Create a HestonModel instance
heston = HestonModel()

# Simulate asset price and volatility paths
paths = heston.simulate_paths(
    initial_price=100,
    mean_reversion=0.1,
    long-term_volatility=0.2,
    volatility_of_volatility=0.3,
    correlation=-0.5,
    maturity=1.0,
    num_time_steps=252,
    num_paths=1000
)

# Visualize the simulated paths
import matplotlib.pyplot as plt

for path in paths:
    plt.plot(path)

plt.xlabel("Time Steps")
plt.ylabel("Asset Price")
plt.title("Heston Model Simulated Paths")
plt.show()
```

## Acknowledgments

This library was inspired by the groundbreaking work of Steven L. Heston and the broader quantitative finance community.

## Support

If you have any questions, bug reports, or feature requests, please open an issue on our [GitHub repository](https://github.com/djinn/explosive).

