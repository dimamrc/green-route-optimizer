# SmartPantry: AI-Powered Household Food Waste Reducer

Final project for the Building AI course.

## Summary

SmartPantry is an AI-powered system that tracks household grocery inventory, predicts expiration dates, and suggests personalized recipes to minimize household food waste and save grocery costs. This is an official Building AI course project.

## Background

Food waste is a major environmental and economic issue worldwide:
* A substantial fraction of municipal solid waste consists of edible food discarded by private households.
* Consumers frequently lose track of expiration dates and store items improperly.
* Reducing food waste directly lowers greenhouse gas emissions and saves household budgets.

My personal motivation stems from observing how easily perishable food is forgotten in everyday life and wanting to apply practical AI methods to make home management effortless.

## How is it used?

The solution is intended for everyday consumers via a mobile or web interface:
1. **Input:** Users scan receipts or capture photos of groceries upon purchase.
2. **Tracking:** The system catalogs items and monitors estimated shelf lives.
3. **Actionable Suggestions:** As expiration dates approach, users receive recipe recommendations based on items that need to be used first.

```python
# Simple demonstration of priority scoring based on shelf-life and quantity
def prioritize_items(inventory):
    # Returns items expiring within 3 days
    return [item['name'] for item in inventory if item['days_remaining'] <= 3]
