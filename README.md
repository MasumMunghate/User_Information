# User_Information

const storedUserInfo = localStorage.getItem("userInformation");: This line tries to retrieve previously stored user information from the browser's local storage. If there's user information stored, it will be assigned to the variable storedUserInfo.
if (storedUserInfo) { ... }: This block checks if there's user information in storedUserInfo (meaning the user has visited the page before and entered their information).
const userInfo = JSON.parse(storedUserInfo);: If there's stored user information, it parses it from a JSON string into a JavaScript object and assigns it to the userInfo variable.
The following lines populate the HTML elements with IDs "first-name", "last-name", "country", "phone-number", "state", "city", and "village" with the corresponding user information values. This effectively displays the user's information on the web page.
function storeUserInfo() { ... }: This is a JavaScript function named storeUserInfo. It's responsible for collecting user information and saving it in local storage.
Inside storeUserInfo(), the code uses prompt to ask the user for their first name, last name, country, phone number, state, city, and village. This information is then stored in an object called userInfo.
localStorage.setItem("userInformation", JSON.stringify(userInfo));: This line stores the userInfo object in local storage under the key "userInformation". It converts the object into a JSON string using JSON.stringify before storing it.
Finally, the same code that displays user information in the HTML elements is called again, updating the displayed information with what the user just entered.
storeUserInfo();: At the end, the storeUserInfo function is immediately called, which means as soon as the page loads, it will ask the user for their information and display it on the page if they've visited before and provided their details.
