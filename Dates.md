Note to Self
* Spent time getting a standard HTML text input of format dd/mm/yyyy to save as a date in Laravel.
* Ended up with the following code in the Objective Model.

```php
    public function setStartDateAttribute($value)
    {
        $this->attributes['start_date'] = Carbon::createFromFormat('d/m/Y', $value)->format('Y-m-d');
    }

    public function setEndDateAttribute($value)
    {
        $this->attributes['end_date'] = Carbon::createFromFormat('d/m/Y', $value)->format('Y-m-d');
    }

    public function setNextReviewDateAttribute($value)
    {
        if ($value) {
            $this->attributes['next_review_date'] = Carbon::createFromFormat('d/m/Y', $value)->format('Y-m-d');
        } else {
            $this->attributes['next_review_date'] = null;
        }
    }
```

* The `next_review_data` was a bit more complex due to the fact that it could be optional.
* All of the above was because Laravel/MySQL stores the date as yyyy-mm-dd.
* Changed the type of the input field from text to date and form still accepted dd/mm/yyyy but passes it back to the server as yyyy-mm-dd.
* Means all the above validation is unnecessary.
* I think this might explain why there weren't more articles on the web explaining how to do the above.