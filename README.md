# Soenneker Semantic Kernel Pool for OpenAI 🎉

![OpenAI Kernel Pool](https://img.shields.io/badge/OpenAI-KernelPool-blue?style=flat&logo=OpenAI)

Welcome to the **Soenneker Semantic Kernel Pool for OpenAI** repository! This project provides OpenAI-specific registration extensions for `KernelPoolManager`, allowing seamless integration with local Large Language Models (LLMs) via Semantic Kernel.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Configuration Options](#configuration-options)
6. [Contributing](#contributing)
7. [License](#license)
8. [Releases](#releases)
9. [Contact](#contact)

## Introduction

The Semantic Kernel is a powerful framework that helps developers build applications using LLMs. This repository extends its capabilities by integrating OpenAI's offerings into the KernelPoolManager. With these extensions, you can manage multiple OpenAI models effectively, optimizing their usage based on your application needs.

## Features

- **OpenAI Integration**: Connect and manage multiple OpenAI models easily.
- **Rate Limiting**: Control the rate at which requests are sent to OpenAI, ensuring compliance with API usage limits.
- **Flexible Options**: Configure various settings to suit your specific requirements.
- **Semantic Kernel Support**: Leverage the full potential of Semantic Kernel while using OpenAI models.

## Installation

To install the package, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/cuti24/soenneker.semantickernel.pool.openai.git
   ```

2. Navigate to the project directory:
   ```bash
   cd soenneker.semantickernel.pool.openai
   ```

3. Install the necessary dependencies:
   ```bash
   dotnet restore
   ```

4. Build the project:
   ```bash
   dotnet build
   ```

## Usage

After installation, you can start using the extensions in your project. Here’s a simple example to get you started:

```csharp
using Soenneker.SemanticKernel.Pool.OpenAI;

var kernelPoolManager = new KernelPoolManager();
kernelPoolManager.RegisterOpenAI("Your-OpenAI-API-Key");

var response = await kernelPoolManager.GetResponseAsync("Your prompt here");
Console.WriteLine(response);
```

This example shows how to register your OpenAI API key and get a response from the model. Adjust the prompt as needed for your application.

## Configuration Options

You can customize the behavior of the `KernelPoolManager` with several options:

- **API Key**: Your OpenAI API key for authentication.
- **Model Selection**: Specify which OpenAI model to use.
- **Rate Limiting**: Set limits on how many requests can be made per minute.

Here’s an example of how to configure these options:

```csharp
var options = new KernelPoolOptions
{
    ApiKey = "Your-OpenAI-API-Key",
    Model = "text-davinci-003",
    RateLimit = 60 // requests per minute
};

kernelPoolManager.Configure(options);
```

## Contributing

We welcome contributions! If you want to help improve this project, please follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/YourFeature
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/YourFeature
   ```
5. Create a pull request.

Please ensure that your code follows the existing style and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

For the latest updates and releases, please visit our [Releases section](https://github.com/cuti24/soenneker.semantickernel.pool.openai/releases). Here, you can find the latest builds and download them for your use.

## Contact

If you have any questions or suggestions, feel free to reach out:

- **Email**: your-email@example.com
- **GitHub**: [your-github-profile](https://github.com/your-github-profile)

Thank you for your interest in the Soenneker Semantic Kernel Pool for OpenAI! We look forward to seeing what you build with it. 

For more information, check the [Releases section](https://github.com/cuti24/soenneker.semantickernel.pool.openai/releases) for updates and downloads.