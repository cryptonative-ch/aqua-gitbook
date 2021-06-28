# Aqua Factory

## Code

[MesaFactory.sol](https://github.com/cryptonative-ch/mesa-smartcontracts/blob/main/contracts/MesaFactory.sol)

## Address

`MesaFactory` is deployed at `xxx` on the Ethereum mainnet, xDai & [Rinkeby](https://rinkeby.etherscan.io/address/0x5C69bEe701ef814a2B6a3EDD4B1652CB9cc5aA6f) testnet. It was built from commit `xxx`.

## Events

#### FactoryInitialized

```text
event FactoryInitialized(
        address feeManager,
        address feeTo,
        address templateManager,
        address templateLauncher,
        uint256 templateFee,
        uint256 feeNumerator,
        uint256 saleFee
    );
```

Emitted by the time the Factory was deployed.

#### TemplateLaunched

```text
event TemplateLaunched(address indexed template, uint256 templateId);
```

Emitted whenever a new template was launched.

* **templateId** indicates which template was used, while **template** is the address of the newly deployed contract

#### SetFeeTo

```text
event SetFeeTo(address indexed feeTo);
```

Emitted whenever the feeManager updates the feeTo

#### SetFeeNumerator

```text
event SetFeeNumerator(uint256 indexed feeNumerator);
```

Emitted whenever the feeManager updates feeNumerator

#### SetSaleFee

```text
event SetSaleFee(uint256 indexed saleFee);
```

Emitted whenever the feeManager updates saleFee

#### SetTemplateFee

```text
event SetTemplateFee(uint256 indexed templateFee);
```

Emitted whenever the feeManager updates templateFee

#### SetFeeManager

```text
event SetFeeManager(address indexed feeManager);
```

Emitted whenever the feeManager updates the feeManager

#### SetTemplateManager

```text
event SetTemplateManager(address indexed templateManager);
```

Emitted whenever the templateManager updates the templateManager

#### SetTemplateLauncher

```text
event SetTemplateLauncher(address indexed templateLauncher);
```

Emitted whenever the templateManager updates the address of the Template Launcher

#### 

## Read-Only Functions

### numberOfSales

```
numberOfSalesfunction factory() external view returns (address);Copy
```

Returns the number of sales launched through the factory

## State-Changing Functions

### initialize

```text
function initialize(
        address _feeManager,
        address _feeTo,
        address _templateManager,
        address _templateLauncher,
        uint256 _templateFee,
        uint256 _feeNumerator,
        uint256 _saleFee
    ) public
```

Initializes the factory right after deployment. Can only be executed one

### launchTemplate

```text
function launchTemplate(uint256 _templateId, bytes calldata _data)
```

Launches a new sale by referencing a templateId to be used and the encoded configuration.

Launches an IDO from a templates. References the **templateId** to be deployed and **data** to configure the template

### setFeeTo

```text
function setFeeTo(address _feeTo) external;
```

Allows the [feeManager](../roles.md#fee-manager) to update the feeTo address, which receives all fees generated on the protocol

Launches an IDO from a templates. References the **templateId** to be deployed and **data** to configure the template

### setFeeNumerator

```text
function setFeeNumerator(uint256 _feeNumerator) external;
```

Allows the [feeManager](../roles.md#fee-manager) to update the feeNumerator which controls the protocol-wide fee

### setSaleFee

```text
function setSaleFee(uint256 _saleFee) external;
```

Allows the [feeManager](../roles.md#fee-manager) to update the saleFee which can be charged for every sale being deployed

### setTemplateFee

```text
function setTemplateFee(uint256 _templateFee) external;
```

Allows the [feeManager](../roles.md#fee-manager) to update the templateFee, which can be charged for installing new templates.

### setFeeManager

```text
function setFeeManager(address _feeManager) external;
```

Allows the [feeManager](../roles.md#fee-manager) to forward the feeManager role to any other address.

### setTemplateManager

```text
function setTemplateManager(address _templateManager) external;
```

Allows the [Template Manager](../roles.md#template-manager) to forward the templateManager role to any other address.

### setTemplateLauncher

```text
function setTemplateLauncher(address _templateLauncher) external;
```

Allows the [Template Manager](../roles.md#template-manager) to plug-in a new templateLauncher.

## Interface

\[...\]

## ABI

\[...\]



