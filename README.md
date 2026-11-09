# **Vehicle Mileage Audit**



Vehicle Mileage Audit is a Sepolia demo that records mileage inspections for one fictional car. Each inspection includes a dashboard reading and two simulated internal module readings. The smart contract flags readings that disagree or fall below the last accepted mileage. An authorized reviewer can record a corrected mileage and a reason. The original readings stay visible in the inspection history.



### Contract



* Network — Ethereum Sepolia
* Contract name — `MileageAudit`
* Contract address — `0xb614E3DB02e7641688E4091E0115d435a5f8Ee14`



### Run the webpage



1\. Open a command window in the project folder.

2\. Run `py -m http.server 8000 --bind 127.0.0.1` and leave that window open.

3\. Open `http://localhost:8000` in Chrome with MetaMask installed.

4\. Click \*\***Connect MetaMask**\*\* and select \*\***Sepolia**\*\* for the page. The dashboard displays the latest accepted mileage and the inspection history.



Anyone can read the history. Submitting an inspection requires the designated reporter wallet and Sepolia test ETH. The reviewer uses Remix to resolve flagged inspections.



### Demo results



The first inspection recorded \*\*50,000 km\*\* on the dashboard and \*\*100,000 km\*\* on both modules. The contract flagged the discrepancy and kept the accepted mileage at \*\*95,000 km\*\* until the reviewer approved \*\*100,000 km\*\*. A second inspection submitted through the webpage recorded \*\*105,000 km\*\* from all three sources. Both inspections remain visible in the history.



The `screenshots` folder shows the Sepolia deployment, wallet connection, and confirmed inspection.

