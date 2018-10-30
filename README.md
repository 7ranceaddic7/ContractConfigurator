# ContractConfigurator
A config file based solution for creating new contracts for Kerbal Space Program.

## How it Works

Contract Configurator exposes various hooks into KSP's contract system through a standard config file syntax. This means that modders using Contract Configurator can create new contracts without writing any code. The config file format has six basic sections (nodes):

  1. CONTRACT_GROUP node - This node provides grouping for multiple Contract Configurator contracts, and allows some common attributes to be set across those groups through the use of a DATA node.
  1. CONTRACT_TYPE node - This is the main node for all Contract Configurator contracts. This node is what defines a contract that will be offered by Contract Configurator.
  1. DATA node - A special node not used by contracts or parameters directly, but provide storage for generic values that can be used as part of expressions.
  1. PARAMETERS node - These are mappings to the stock ContractParameter classes which specify what the player has to do to complete the contract.
  1. REQUIREMENTS node - This is what is required before the contract will show up. Most of the ProgressTracking information is supported, along with a few other things.
  1. BEHAVIOUR node - This node defines a contract behaviour - any behaviour that is at the contract level. These can provide functionality for parameters, be used to persist data from contract to contract or any number of other things.
  
If the provided parameters and requirements aren't enough, Contract Configurator is extensible. New parameters and requirements can be added in as little as a dozen lines of code.
