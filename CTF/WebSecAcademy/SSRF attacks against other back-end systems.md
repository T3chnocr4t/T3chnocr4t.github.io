***
# SSRF
### Lab:# SSRF attacks against other back-end systems

Let’s go through this, guys. This is a Web Security Academy lab on [SSRF attacks against other back-end systems](https://portswigger.net/web-security/learning-paths/server-side-vulnerabilities-apprentice/ssrf-apprentice/ssrf/lab-basic-ssrf-against-backend-system). This lab has a stock check feature which fetches data from an internal system. Our task is to solve the lab by using the stock check functionality to scan the internal 192.168.0.X range for an admin interface on port 8080, and then use it to delete the user Carlos.

![server-side request forgery](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/533c6a2f-d600-44a3-87dc-e67322f803b6)

### End Goal:#
- Access the admin panel and delete user carlos

### Testing For VUlnerabilities:#
- Let's check the functionality of the web app.

![21](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/fd70031f-f226-412a-ac56-bea60b14a136)

- There are many products listed in the web app. Let’s visit a product and click "Check Stock." In Burp, let’s check each request we make. Check the Proxy tab, and we can see our request. Let’s send it to the Repeater tab.

![22](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/04b21d33-6704-4031-8ad5-7cae7ca2561b)

- Modify the stockApi parameter to `http://192.168.0.x:8080/admin` and send it to the Intruder tab. Highlight the x in the stockApi parameter in Intruder under the Positions tab. We can see that the x is automatically set as a payload position, indicated by two § symbols. Select the attack type as Sniper.

![23](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/4c08d2ac-4408-4ebb-9146-1bcd9f243bbb)

- After that, go to the Payloads tab and make sure that the number payload type is selected. Enter a range from 1 to 256, and then start the attack.

![24](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/f7b8ca44-f04a-40c0-9584-e1d03ece1e23)

- When the attack is complete, go to the Results tab and check the Length column. Notice that one of the entries is longer than the others, and only one status code is different, which is 200. Showing and admin interface.

![26](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/574c4af6-bcd9-4c19-b22a-62fa09833b84)

- Send it to the Repeater tab and specify the URL path in the stockApi parameter to delete the user Carlos

![dancing-rick-and-morty](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/d9978028-ca44-41b4-9ca9-09e416a71fb8)

That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)

