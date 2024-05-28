# Working with Azure AI projects on your compute instance

## Get started with the Azure AI Folder Hierarchy

The Azure AI folder hierarchy (`afh`) is designed to orient you within your current working context, and help you work with your code, data and shared files most efficiently. This `afh` directory houses your Azure AI projects, and each specific project's folder has a `code`, `data` and `shared` folder.

Files, folders, and repos you store in your project folder persist across compute instance restarts but are lost if the machine is deleted.

### The `code` and `data` folders

- Use `code` for working with git repositories and private code files
- Use `data` for storing private data files

The `code` folder is where we recommend you clone your git repositories, or otherwise bring in or create your code files. This is a storage location directly on your compute instance, and will be performant for large repositories. We recommend you use the `data` folder to store and reference local or private data in a consistent way.

### The `shared` folder

- Use `shared` for working with a project's shared files and assets
- Use `shared\Users\{user-name}\promptflow` to reference and edit prompt flows

The `shared` folder is where you will find the project's shared files and assets, including prompt flows that are being developed in the Azure AI Studio. To find specific files or flows, navigate to the relevant user folder. Flows will be in the `promptflow` folder.

## Get started with the AI Studio custom container for VS Code

For those that launched VS Code from the Azure AI Studio, you are remotely connected to a custom container running on your compute instance. The file explorer is loaded in a dedicated folder for the project you were working on in the Azure AI Studio. This development environment comes pre-configured with the Azure AI SDK, the Azure AI CLI, and the Prompt flow SDK and CLI.

To set up these capabilities in your local environment instead, or to learn more, follow steps here: [Azure AI SDK](<https://aka.ms/aistudio/docs/sdk>).

### The Azure AI SDK

To get started with the AI SDK, we recommend the [aistudio-copilot-sample repo](https://github.com/azure/aistudio-copilot-sample) as a comprehensive starter repository that includes a few different copilot implementations. For the full list of samples, check out the [Azure AI Samples repository](https://github.com/azure-samples/azureai-samples).

1. Open a terminal
1. Clone a sample repo into your project's `code` folder. You may be prompted to authenticate to Github

```bash
cd code
git clone https://github.com/azure/aistudio-copilot-sample
```

3. If you have existing notebooks or code files, you can import `import azure.ai.generative` and use intellisense to browse capabilities included in that package

### The Azure AI CLI

If you prefer to work interactively, the AI CLI has everything you need to build generative AI solutions.

1. Open a terminal to get started
1. `ai help` will guide you through CLI capabilities
1. `ai init` will configure your resources in your development environment

### Working with prompt flows

You can use the Azure AI SDK and AI CLI to create, reference and work with the flows.

Prompt flows already created in the Azure AI Studio can be found at `shared\Users\{user-name}\promptflow`. You can also create new flows in your `code` or `shared` folder using the CLIs and SDKs.

1. To reference an existing flow using the Azure AI CLI, use `ai flow invoke`
1. To create a new flow using the Azure AI CLI, use `ai flow new`

For prompt flow specific capabilities that are not present in the AI SDK and CLI, you can work directly with the Prompt flow CLI or SDK, or the Prompt flow VS Code extension (all pre-installed in this environment). See [prompt flow capabilities](<https://microsoft.github.io/promptflow/reference/index.html>) for more details.

### Client application development

For client app developers seeking cross-language compatibility and seamless integration of OpenAI capabilities, explore the Azure AI Hub at <https://aka.ms/azai>. Discover app templates and SDK samples in your preferred programming language.
