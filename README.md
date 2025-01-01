# Tailwind CSS Purge Option Conflict with Dynamic Classes

This repository demonstrates a bug and its solution related to Tailwind CSS's purge option and dynamically generated class names. The bug occurs when Tailwind's purge functionality removes CSS rules because it doesn't recognize dynamically generated classes. This results in missing styles even though the class names and configurations appear correct.

## Bug Description

The issue involves a conflict between Tailwind's `purge` option (or its `content` option in Tailwind CSS v3) and the use of dynamic class names in the application. Even with properly named classes and a seemingly accurate `tailwind.config.js` file, the styles won't apply because the purge process eliminates the corresponding CSS rules due to a lack of recognition of these dynamic class names.

## Bug Reproduction

1. Clone this repository.
2. Install dependencies using `npm install`.
3. Run the development server (instructions may vary depending on your project setup).
4. Observe that the dynamically styled elements do not have the expected Tailwind styles applied.

## Solution

The solution involves modifying the `tailwind.config.js` file's `content` array to include the files where dynamic classes are generated. This ensures the purge process includes these classes and prevents the removal of necessary CSS rules.  See the `bugSolution.js` file for a demonstration.