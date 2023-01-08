# datebook sveltekit issues

The project will run fine when you run `npm run dev` and build locally.

However when you run `npm run build && npm run preview` you will get a 500 internal server error and the following issue will appear in the terminal:

```
import { GoogleCalendar, OutlookCalendar, YahooCalendar, ICalendar } from "datebook";
         ^^^^^^^^^^^^^^
SyntaxError: Named export 'GoogleCalendar' not found. The requested module 'datebook' is a CommonJS module, which may not support all module.exports as named exports.
CommonJS modules can always be imported via the default export, for example using:

import pkg from 'datebook';
const { GoogleCalendar, OutlookCalendar, YahooCalendar, ICalendar } = pkg;

    at ModuleJob._instantiate (node:internal/modules/esm/module_job:124:21)
    at async ModuleJob.run (node:internal/modules/esm/module_job:190:5)
```

If you copy the contents of the minified `datebook.esm.min.js` locally and import it it will work fine. Hope this helps troubleshoot the issues! 

