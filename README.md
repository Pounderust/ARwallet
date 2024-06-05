# ARwallet
Some wallets may be difficult to use for some users due to limited internal memory requiring the download of an apk android version etc.  This makes it very difficult for some people when &lt;connect to dapps> purchasing via the Defi platform/purchasing NFT assets  Development here still requires other literature.Maybe the <web version> 
can help make things easier for users

//connecting the wallet to the app, working UI components, and hooks that allow building a custom Connect Wallet.

import {
  Provider,
  ConnectButton,
} from "web/react";
import {
  createWallet,
  walletConnect,
  inAppWallet,
} from "web/wallets";

const client = createwebClient({
  clientId: "CLIENT_ID",
}); 

const wallets = [
  createWallet(" "),
  createWallet(" "),
  walletConnect(),
  inAppWallet({
    auth: {
      options: ["phone"],
    },
  }),
];

export default function App() {
  return (
    <webProvider>
      <ConnectButton
        client={client}
        wallets={wallets}
        theme={"dark"}
        connect={{
          size: "wide",
          title: "ARBEEV Wallet",
          titleIcon: " ",
          welcomeScreen: {
            title:
              "Enter your phone number to create an account",
            subtitle: "connection to start",
          },
          showwebBranding: false,
        }}
      />
    </webProvider>
  );
}
