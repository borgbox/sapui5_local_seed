1. Open a shell or command prompt and go to the folder containing the extracted app. Run npm install to install all dependencies (ignore all deprecation warnings). 

2. Run ui5 init to generate a ui5.yaml file 

3. Run ui5 build --all to start the build process that creates the preload bundles. Wait until the build is ready. 

4. Install a small web server to serve our app. npm install --global serve@6

5. Open a second shell or command prompt and go to the folder containing the extracted app.

6.  Adjust user and password in package.json and Start the CORS proxy in the second Shell npm run localproxy

7. Start the webserver in the first Shell serve ./dist

8. Open a browser, and open http://localhost:5000/index.html

To build a self contained app

1. Stop the web server in the first shell with CRTL+C, but keep the CORS proxy in the second Shell running.

2. Run ui5 build selfcontained --all in the first Shell.

3. Start the web server in the first shell with serve ./dist

4. Open a browser, and open http://localhost:5000/index.html