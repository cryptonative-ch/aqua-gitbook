# Template Launcher

## Code

[TemplateLauncher.sol](https://github.com/cryptonative-ch/mesa-smartcontracts/blob/main/contracts/templates/TemplateLauncher.sol)

## Address

`TemplateLauncher` is deployed at `xxx` on the Ethereum mainnet, xDai & Rinkeby testnet. It was built from commit `xxx`.

## Events

#### TemplateLaunched

```text
event TemplateLaunched(address indexed sale, uint256 templateId);
```

Emitted whenever a new template get's launched

#### TemplateAdded

```text
event TemplateAdded(address indexed template, uint256 templateId);
```

Emitted whenever a new template was installed.

#### TemplateRemoved

```text
event TemplateRemoved(address indexed template, uint256 templateId);
```

Emitted whenever a new template was uninstalled by the Template Manager.

#### TemplateVerified

```text
event TemplateVerified(address indexed template, uint256 templateId);
```

Emitted whenever a new template was verified by the Template Manager.

#### UpdatedTemplateRestriction

```text
event UpdatedTemplateRestriction(bool restrictedTemplates);
```

Emitted whenever the Template Manger updates the Template Restrictions.

## Read-Only Functions

#### getTemplate

```
function getTemplate(uint256 _templateId);
```

Returns the contract address for a provided TemplateId.

## State-Changing Functions

#### launchTemplate

```text
function launchTemplate(uint256 _templateId, bytes calldata _data)
```

Launches a Template from a templates. References the **templateId** to be deployed and **data** to configure the template

