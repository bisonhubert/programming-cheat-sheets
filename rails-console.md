start a Rails console
rails c

start a sandbox Rails console
rails c --sandbox

start heroku qa server from terminal
```bash
heroku run --app pillow-qa rails console
```

update attribute and bypass validation
```bash
$ resource.update_attribute :column_name, 3
```

update cleaning status by cleaning id to pending
```bash
Cleaning.find(69377).update_attribute(:status, 0)
```

find acknowledged or started cleanings
```bash
fellow = Fellow.find(531)
activity = fellow.activities.find_by(status: 1)
activity = fellow.activities.find_by(status: 4)
```

Cleaning ID 79724
Property ID 7798
Cleaning for 1621 North 55th St, Seattle WA
Cleaning.find(79724).update_attribute(:status, 0)

Cleaning ID 69957
Property ID 4950
Cleaning for 5625 12th Ave NE, Unit B
Cleaning.find(69957).update_attribute(:status, 0)

Cleaning.find(79724).update_attribute(:status, 0) && Cleaning.find(69957).update_attribute(:status, 0)
