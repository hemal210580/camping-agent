# Camping agent: Yosemite Valley + Lake Tahoe, summer 2027

[camply](https://github.com/juftin/camply) searches Recreation.gov and ReserveCalifornia
and sends a phone alert (ntfy) when a matching campsite opens. Booking is done by hand.

| Config | Watches |
|---|---|
| `yosemite_valley_2027.yaml` | Upper, Lower, North Pines |
| `tahoe_forest_2027.yaml` | Fallen Leaf, Nevada Beach, William Kent, Kaspian, Meeks Bay, Zephyr Cove |
| `tahoe_state_parks_2027.yaml` | D.L. Bliss, Emerald Bay (Eagle Point), Sugar Pine Point |

All: arrivals Jun 1 – Sep 7, 2027, 2 consecutive nights.

## Where it runs
- **GitHub Actions** (`.github/workflows/camply.yml`): every ~10 minutes, 24/7.
  Needs the repository secret `NTFY_TOPIC`.
- **Windows PC** (`AI-projects\camping-agent`): every 5 minutes while signed in
  (weekday mornings). Best coverage for 7 AM release mornings.

## Change the search
Edit a YAML file here (dates, `nights`, `weekends: true`, campgrounds) and commit.
Copy the same change to the PC folder and run `restart_camply.bat` there.

## Pause
Actions tab → camply campsite watcher → ⋯ → Disable workflow.
