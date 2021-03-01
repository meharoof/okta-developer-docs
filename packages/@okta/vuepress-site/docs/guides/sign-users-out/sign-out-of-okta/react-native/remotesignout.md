### Clear the Okta session

Clear the browser session and clear the app session (stored tokens) in memory. Fires an event once a user successfully logs out.

> Note: This method apply for browser-sign-in scenario only. Use a combination of revokeToken (optional) and clearTokens methods to signOut when use custom-sign-in.

browser-sign-in example:

```javascript
import { signOut } from '@okta/okta-react-native';

signOut();
```

custom-sign-in example:

```javascript
import { revokeAccessToken, revokeIdToken, clearTokens } from '@okta/okta-react-native';

await revokeAccessToken(); // optional
await revokeIdToken(); // optional
clearTokens()
    .then(() => { })
    .catch(e => { });
```