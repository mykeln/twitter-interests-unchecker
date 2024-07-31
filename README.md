# Cleanse your algo!

If you visit https://x.com/settings/your_twitter_data/twitter_interests you'll see a bunch of crap that the algorithm thinks you're interested in. This script unchecks them all.

1. On x.com, go to settings and privacy -> privacy and safety -> content you see -> interests
2. Paste this code into the console:

```
(function() {
  // Select all checkboxes on the page
  const allCheckboxes = document.querySelectorAll('input[type="checkbox"]');
  
  // Log the number of checkboxes found
  console.log(`Found ${allCheckboxes.length} checkboxes.`);
  
  // Iterate through the NodeList and simulate a click on each checkbox
  allCheckboxes.forEach(checkbox => {
    if (checkbox.checked) {
      checkbox.click();
      console.log(`Clicked checkbox:`, checkbox);
    }
  });
})();
```
