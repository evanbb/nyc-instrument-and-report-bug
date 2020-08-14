# NYC Reporting and Source Map Bug

## Repro steps

1. clone this repo
2. `npm i`
3. `npm run build`
4. `cd build`
5. `npx nyc ./static ./static-i`
6. rename `static` to `static-o`, `static-i` to `static`
7. `npx serve`
8. open chrome to `localhost:5000`
9. in dev tools console, `JSON.stringify(__coverage__)`
10. copy data into `.nyc_output/out.json`
11. `npx nyc report --reporter=html`
12. open `coverage/index.html`
13. report here looks good
14. click into any of the `.js` files
15. cry a little