# VoltTest

**High-Performance Load Testing Made Simple**

VoltTest is a powerful, cross-platform performance testing framework that combines the ease of use of modern programming languages with the raw performance of Go. Our unique architecture enables developers to write intuitive test scenarios while leveraging Go's superior concurrency and performance characteristics for actual load generation.

## 🚀 Why VoltTest?

- **📝 Write Once, Run Anywhere**: Create tests in your preferred language with our SDKs
- **⚡ Go-Powered Engine**: High-performance load generation with true parallel execution
- **🔄 Real-time Results**: Live metrics and progress tracking during test execution
- **📊 Comprehensive Analytics**: Detailed performance metrics and response time analysis
- **🌐 Cross-Platform**: Supports Windows, Linux, and macOS
- **🎯 Developer-Friendly**: Fluent APIs and intuitive test configuration

## 🏗️ Architecture

VoltTest uses a hybrid architecture where:

1. **SDKs** provide developer-friendly APIs for test definition
2. **Go Engine** handles the actual load generation and execution
3. **Communication Layer** streams real-time results back to your application

This approach gives you the best of both worlds: easy test creation and maximum performance.

## 📦 Available SDKs

### PHP SDK
[![PHP Version](https://img.shields.io/badge/PHP-8.0%2B-blue)](https://github.com/volt-test/php-sdk)
[![License](https://img.shields.io/badge/License-MIT-green)](https://github.com/volt-test/php-sdk/blob/main/LICENSE)

Write performance tests with PHP's familiar syntax and extensive ecosystem.

```php
$test = new VoltTest('API Load Test', 'Testing user authentication flow');

$test->setVirtualUsers(100)
     ->setDuration('5m')
     ->setRampUp('30s');

$scenario = $test->scenario('User Login')
    ->autoHandleCookies();

$scenario->step('Login')
    ->post('/api/login', '{"email": "user@test.com", "password": "secret"}')
    ->header('Content-Type', 'application/json')
    ->extractFromJson('token', 'data.access_token')
    ->validateStatus('login_success', 200);

$result = $test->run(true);
echo "Success Rate: " . $result->getSuccessRate() . "%\n";
```

**[📖 PHP SDK Documentation](https://php.volt-test.com)**

### Coming Soon

- **JavaScript/Node.js SDK** - Write tests with JavaScript
- **Python SDK** - Leverage Python's simplicity for load testing
- **Java SDK** - Enterprise-ready performance testing

## 🔧 Core Features

### Virtual Users & Scenarios
- Configure multiple virtual users with realistic behavior patterns
- Weight scenarios for complex traffic simulation
- Support for data-driven testing with CSV files

### Request Capabilities
- Full HTTP method support (GET, POST, PUT, DELETE, etc.)
- Custom headers and authentication
- Request/response body manipulation
- Cookie handling and session management

### Data Extraction & Validation
- **JSON Path**: Extract data from JSON responses
- **Regex**: Pattern-based data extraction
- **Headers**: Extract values from response headers
- **Cookies**: Session and state management
- **HTML**: CSS selector-based extraction

### Performance Metrics
- Response time statistics (min, max, avg, percentiles)
- Request success/failure rates
- Requests per second (RPS)
- Custom validation rules

### Real-time Monitoring
- Live progress tracking
- Streaming metrics during execution
- Debug mode for request/response inspection

## 🏃‍♂️ Quick Start

1. **Choose your SDK** (currently PHP, more coming soon)
2. **Install the SDK** using your language's package manager
3. **Write your first test** following the SDK documentation
4. **Run and analyze** your performance tests

## 📊 Example Results

```
Test Metrics Summary:
===================
Duration:     5m 24.5s
Total Reqs:   50,000
Success Rate: 99.8%
Req/sec:      154.2
Success Requests: 49,900
Failed Requests: 100

Response Time:
------------
Min:    12ms
Max:    2.4s
Avg:    245ms
Median: 180ms
P95:    650ms
P99:    1.2s
```

## 🛠️ Installation

### PHP SDK
```bash
composer require volt-test/php-sdk
```

### Manual Binary Installation
Download the latest binary for your platform from our [releases page](https://github.com/volt-test/binaries/releases).

## 📚 Documentation

- **[Getting Started Guide](https://php.volt-test.com)**
- **[Examples & Tutorials](https://php.volt-test.com/blog)**

## 🤝 Contributing

We welcome contributions! Whether you're:
- 🐛 Reporting bugs
- 💡 Suggesting new features
- 📝 Improving documentation
- 🔧 Contributing code


## 🎯 Use Cases

- **API Load Testing**: Test REST APIs under various load conditions
- **Web Application Testing**: Simulate real user behavior and traffic patterns
- **Performance Regression Testing**: Ensure new releases don't degrade performance

## 📈 Roadmap

- [ ] JavaScript/Node.js SDK
- [ ] Python SDK
- [ ] Java SDK
- [ ] Web UI for test management
- [ ] Cloud-hosted testing service
- [ ] Advanced reporting and analytics
- [ ] Distributed load testing
- [ ] Integration with popular CI/CD platforms

## 💬 Community

- **[GitHub Discussions](https://github.com/orgs/volt-test/discussions)** - Ask questions and share ideas
- **[Issues](https://github.com/volt-test/php-sdk/issues)** - Report bugs and request features

## 🙏 Acknowledgments

Special thanks to all contributors and the open source community that makes projects like this possible.
