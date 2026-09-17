# Cab Ledger

A mobile-friendly first version for London cab drivers to record shifts, jobs, mileage, takings and estimated running costs.

Use it at https://ali1989ec-ship-it.github.io/cab-ledger/ . GitHub Pages publishes the `dist` folder when changes are pushed to `main`.

## Run

Serve the `dist` directory with any local static HTTP server, for example `python3 -m http.server 8000 --directory dist`, then open `http://localhost:8000`. Location needs HTTPS on a real device. No installation or secret configuration is required.

## How it works

Set your vehicle and estimated cost per mile. Start a shift with your odometer reading, optionally start and finish individual jobs, and enter the final mileage, takings and expenses when you end the shift. The summary uses odometer readings for completed shifts. Optional GPS is only an estimate while the page is active; it is never used as the final distance. No raw location points are saved.

Records stay in this browser's local storage. Export a CSV to back them up; clearing browser storage removes the records. There are no accounts or cross-device sync in this first version. Estimated costs are based on user-supplied rates and do not include tax or unrecorded costs. Do not use the controls while driving.

## Checks

Run `node --check dist/app.js` and `node --check dist/model.js`, then exercise the full shift flow in a browser. The site has no build step.

## Next steps

Test with real cab drivers and phones before adding a backend or paid features. A mobile app will be needed if dependable background location recording becomes essential.
