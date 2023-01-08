### Install [Yarn or Npm]
    ~ $ yarn install
    
    ## Replace - env.example -> .env
##### Run dev 
    ~ $ yarn start:dev 
##### Run Production
       ~ $ yarn build
       ~ $ yarn start 
    

Script in package.json:

    "start:dev": "nodemon", // Run dev
    "build": "next build && tsc --project tsconfig.server.json", // Build Before Run Production
    "start": "cross-env NODE_ENV=production node dist/index.js", // Run on Production 
    "lint": "eslint './{src,pages,server}/**/*' --ext .tsx,.ts",
    "pretty": "prettier --write --config .prettierrc.js {src,pages,server}/**/*.{ts,tsx}",// Format Code
    "format": "npm run lint -- --fix", // Fix Eslint
    "analyze": "cross-env BUNDLE_ANALYZE=both npm run build", // Phân tích dung lượng thư viện
    "export": "cross-env NODE_ENV=production next export", // Build ra file tĩnh
    "cli": "pankod-cli add" // CLi add new Page , Component
