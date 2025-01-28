// Function to extract the city name from the URL
function getLocationFromURL() {
  const path = window.location.pathname; // Get the URL path
  const segments = path.split('/').filter(Boolean); // Split the path into segments
  if (segments.length > 0) {
    const cityName = segments[0].replace(/-/g, ' '); // Replace dashes with spaces
    console.log("Extracted City Name:", cityName); // Log the extracted city name
    return cityName;
  }
  console.log("No city found in the URL path. Using fallback value.");
  return 'Your Location'; // Default fallback value
}

// Dynamically replace the {location} placeholder
document.addEventListener('DOMContentLoaded', () => {
  const cityName = getLocationFromURL(); // Extract city name
  console.log("City Name to Replace {location}:", cityName); // Log the city name to be used

  // Get the full HTML content
  const htmlContentBefore = document.body.innerHTML;
  console.log("Full HTML Content Before Replacement:", htmlContentBefore); // Log the HTML before replacement

  // Replace all instances of {location} with the city name
  const htmlContentAfter = htmlContentBefore.replace(/{location}/g, cityName);
  console.log("Full HTML Content After Replacement:", htmlContentAfter); // Log the HTML after replacement

  // Update the page content
  document.body.innerHTML = htmlContentAfter;
});
