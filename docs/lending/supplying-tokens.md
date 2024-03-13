<h1>Supplying Assets</h1>


## **How do ERC-4626 Vaults work?**

Liquidity for borrowers is provided in ERC-4626 vaults. For detailed documentation on how they work, please check out the official [Ethereum documentation](https://ethereum.org/de/developers/docs/standards/tokens/erc-4626/) or visit the [technical docs of Curve](https://docs.curve.fi/lending/contracts/vault/).

!!!danger "Risks"
    Add a risk disclaimer here.


---


## **Depositing and Withdrawing Assets**

In order to supply tokens to the vault, the user must specify the amount of underlying tokens to add. Underlying tokens are referred to as the asset in the vault, which is the asset that's borrowed. When depositing, the UI previews the amount of shares to receive and projects the lend APY after the deposit. For depositing, there is no cap. Users can deposit as much as they want.

If a user already deposited some shares, they can withdraw the desired amount under the withdraw tab. The desired amount of underlying assets to be withdrawn needs to be specified. Here as well, the UI previews the amount of shares to be burned in order to receive the underlying tokens. When desired, users can stake their vault shares into the corresponding gauge (if there is one) using the "Stake" tab. Liquidity gauges of the vaults can be added to the GaugeController in order to be eligible to receive CRV emissions or external rewards can be added to the gauge by the deployer.

*Disclaimer: The figure below is just an embedded UI. It is highly recommended to visit: [https://lend.curve.fi/#/ethereum/markets](https://lend.curve.fi/#/ethereum/markets)*

<iframe src="https://lend.curve.fi/#/ethereum/markets/one-way-market-2/vault/deposit" width="100%" height="500px"></iframe>


!!!tip "Lending Rates when Depositing or Withdrawing Assets"
    When depositing underlying assets into the vault, the lending rate may decrease depending on the amount of assets added. The reason for this is that when supplying additional assets, the market's utilization rate will decrease (as there are now more assets to borrow from), which simultaneously decreases the borrow rate. When the borrow rate decreases, the lending rate decreases as well.

    Vice versa: Withdrawing assets from the vault reduces the total amount of assets. This drives the utilization rate up, which increases the borrow rate and therefore also the lending rate.


---


*Having "Advanced Mode" enabled adds a full overview of the vault.*

<figure markdown="span">
  ![](../images/lending/supply_overview.png){ width="600" }
  <figcaption></figcaption>
</figure>


*If a user has shares, the user can view their personal vault information on the "Your Details" tab.*

<figure markdown="span">
  ![](../images/lending/supply_yourdetails.png){ width="600" }
  <figcaption></figcaption>
</figure>