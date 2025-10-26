# 🎯 Single Server Queue Simulation

A beautiful, interactive web-based discrete-event simulation for analyzing single-server queue systems using exponential interarrival and service time distributions.


## ✨ Features

- **📊 Real-time Simulation** - Run queue simulations with customizable parameters
- **📈 Interactive Charts** - Visualize waiting times and system times with Chart.js
- **🎨 Beautiful UI** - Modern gradient design with smooth animations
- **🌓 Dark/Light Theme** - Toggle between themes with automatic chart updates
- **📱 Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- **📋 Detailed Statistics** - Comprehensive metrics and tabular results
- **🚀 Zero Dependencies** - Self-contained HTML file, runs entirely in the browser

## 🎮 Demo

Simply open the HTML file in any modern web browser to start simulating!

## 📖 What is Queue Simulation?

Queue simulation models real-world waiting line scenarios like:
- Customer service centers
- Hospital emergency rooms
- Bank teller lines
- Call center operations
- Manufacturing processes

The simulation uses **exponential distributions** for:
- **Interarrival times** (λ - arrival rate)
- **Service times** (μ - service rate)

## 🛠️ How to Use

### Basic Usage

1. **Open the file** - Double-click the HTML file or open it in your browser
2. **Set parameters**:
   - **Arrival Rate (λ)**: Average number of customers arriving per time unit
   - **Service Rate (μ)**: Average number of customers served per time unit
   - **Number of Customers**: Total customers to simulate
3. **Run Simulation** - Click the "🚀 Run Simulation" button
4. **Analyze Results** - View metrics, charts, and detailed tables

### Parameter Guidelines

- **λ < μ** → Stable system (recommended for meaningful results)
- **λ ≥ μ** → Unstable system (queue grows indefinitely)
- **Utilization (ρ)** = λ/μ should be < 1 for stable queues

### Example Scenarios

**Fast Service, Low Traffic**
```
Arrival Rate (λ): 1.0
Service Rate (μ): 2.5
Customers: 20
Expected Result: Low waiting times, high efficiency
```

**Busy System**
```
Arrival Rate (λ): 2.0
Service Rate (μ): 2.5
Customers: 50
Expected Result: Moderate waiting times, higher utilization
```

**Near Capacity**
```
Arrival Rate (λ): 2.4
Service Rate (μ): 2.5
Customers: 100
Expected Result: Long waiting times, very high utilization
```

## 📊 Understanding the Results

### Summary Statistics

- **Avg Waiting Time** - Average time customers wait in queue before service
- **Avg Service Time** - Average time customers spend being served
- **Avg System Time** - Average total time in system (waiting + service)
- **Utilization** - Server busy percentage (λ/μ)
- **Total Time** - Total simulation duration

### Charts

1. **Waiting Time Chart** - Shows how waiting time varies per customer
2. **System Time Chart** - Displays total time in system for each customer

### Detailed Table

View per-customer metrics:
- Arrival time
- Service start time
- Service duration
- Departure time
- Time spent waiting
- Total system time

### Algorithm

The simulation uses a **discrete-event approach**:

1. Generate exponential random variates for interarrival and service times
2. Calculate cumulative arrival times
3. For each customer:
   - Service start = max(arrival time, previous departure)
   - Waiting time = service start - arrival time
   - Departure = service start + service time
   - System time = departure - arrival time
4. Calculate aggregate statistics

### Technologies Used

- **HTML5** - Structure and layout
- **CSS3** - Modern styling with CSS variables and gradients
- **Vanilla JavaScript** - Simulation logic and interactivity
- **Chart.js** - Data visualization
- **Google Fonts (Inter)** - Typography

## 🎓 Educational Use

Perfect for:
- **Operations Research** courses
- **Probability & Statistics** classes
- **Industrial Engineering** programs
- **Computer Science** simulation courses
- **Business Analytics** training

## 🤝 Contributing

Feel free to enhance this simulation by:
- Adding more queue disciplines (LIFO, Priority)
- Implementing multiple servers
- Adding more distributions (Normal, Uniform)
- Creating export functionality for results
- Adding animation of queue behavior

## 📄 License

MIT License - Feel free to use, modify, and distribute.

## 🙏 Acknowledgments

- Chart.js for powerful visualization
- The queueing theory community
- Exponential distribution mathematics

## 📞 Support

For issues or questions:
- Check the console for error messages
- Ensure JavaScript is enabled in your browser
- Verify you're using a modern browser version

**Made with ❤️ for simulation enthusiasts**

Happy Simulating! 🚀