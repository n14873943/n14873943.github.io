// Find the email input field using XPath
var emailInput = document.evaluate('//*[@id="identifierId" or @id="Email"]', document, null, 
                        XPathResult.FIRST_ORDERED_NODE_TYPE, null).singleNodeValue;

// Check if the input field exists
if (emailInput) {
    // Set the value of the email input field
    emailInput.value = 'radiantserenade42@allison.harith.app'; // Replace 'example@email.com' with your desired email
    
    // Dispatch an 'input' event to simulate typing
    var inputEvent = new Event('input', { bubbles: true });
    emailInput.dispatchEvent(inputEvent);
} else {
    console.error('Email input field not found!');
}

// Find the 'Next' button and click it
var nextButton = document.evaluate('//*[@id="identifierNext"]/div/button/span or //*[@id="next"]', document, null, 
                        XPathResult.FIRST_ORDERED_NODE_TYPE, null).singleNodeValue;

// Check if the button exists
if (nextButton) {
    // Click the 'Next' button
    nextButton.click();
} else {
    console.error('Next button not found!');
}

// Wait for 6 seconds before typing the password
setTimeout(function() {
    // Find the password input field using XPath
    var passwordInput = document.evaluate('//*[@id="password"]/div[1]/div/div[1]/input or //*[@id="Passwd"]', document, null, 
                            XPathResult.FIRST_ORDERED_NODE_TYPE, null).singleNodeValue;
    
    // Check if the input field exists
    if (passwordInput) {
        // Set the value of the password input field
        passwordInput.value = 'Haris123@'; // Replace 'yourpassword' with your desired password
        
        // Dispatch an 'input' event to simulate typing
        var inputEvent = new Event('input', { bubbles: true });
        passwordInput.dispatchEvent(inputEvent);
    } else {
        console.error('Password input field not found!');
    }

    // Find the 'Next' button after entering the password and click it
    var passwordNextButton = document.evaluate('//*[@id="passwordNext"]/div/button/span or //*[@id="submit"]', document, null, 
                                XPathResult.FIRST_ORDERED_NODE_TYPE, null).singleNodeValue;
    
    // Check if the button exists
    if (passwordNextButton) {
        // Click the 'Next' button
        passwordNextButton.click();
    } else {
        console.error('Password Next button not found!');
    }
}, 6000); // Wait for 6 seconds (6000 milliseconds) before executing the password typing and clicking logic

// Wait for 3 seconds before opening the YouTube channel switcher URL
setTimeout(function() {
    // Check if the current URL matches the desired pattern
    if (window.location.href === "https://www.youtube.com/channel_switcher") {
        // Open a new URL in the current tab
        window.location.href = 'https://www.example.com'; // Replace 'https://www.example.com' with your desired URL
    }
}, 10000); // Wait for 3 seconds (3000 milliseconds) before checking the URL pattern and potentially opening a new URL
