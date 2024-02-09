# AWS CDK LLRT Function construct

This is a CDK construct library that aims to accelerate your experiment on [LLRT](https://github.com/awslabs/llrt), a lightweight JavaScript runtime for AWS Lambda.

## Usage
Install it via npm:

```sh
npm install cdk-llrt-function
```

Then you can just specify an entry point for the function.

```ts
import { LlrtFunction } from 'cdk-llrt-function';

const handler = new LlrtFunction(this, 'Handler', {
    entry: 'lambda/index.ts',
});
```

If you are already using `NodejsFunction` construct, you should be able to just replace it to `LlrtFunction`.

> [!WARNING]
> LLRT is currently experimental and not fully compatible with Node.js. You should expect some trial and errors to use LLRT with your existing code.