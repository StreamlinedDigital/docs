# News Articles

## User Story
 - As a **user**, I want to **get critical high level engaging news about Intelligrated**, so that **I can stay up to date on what is happening at Intelligrated**.

## Lists/Views
| View        | Details           |
| -------------    |-------------
| List                  | https://ihomedev.intelligrated.com/Lists/Articles        
| Approval View         | https://ihomedev.intelligrated.com/Lists/Articles/mod-view.aspx        
| Homepage View         | https://ihomedev.intelligrated.com/default.aspx                      
| All News View         | https://ihomedev.intelligrated.com/default.aspx#/news                      
| Article Detail View   | https://ihomedev.intelligrated.com/default.aspx#/article/2


## Fields
| Field        | Details           |
| -------------    |-------------
| `Title`          | right-aligned                       
| `Preview_img`    | a) Visible on the homepage & article detail view. b) The image aspect ratio should maintain across all views  c) The app is set to clip extra pixels from view to maintain the aspect ratio
| `Published_at`   | *Not sure if this is still need*
| `Body`           | the content of the article  
| `Sort_Order`     | a) Only the top 6 approved items will be returned sorted by sort_order b) The sort order must be maintained by the site owner                            
| `ID`             | The url structure is determined by the ID

## Sort & Filter
- Only the top 6 articles using the `Sort_Order` field in ascending order

## Approval Workflow
- Only `approved` articles are visible through the application
- All new articles are set to draft by default and must be approved before they are visible
- Anytime an article is updated it reverts to "draft mode again until it is approved"
   - This is set by default by Sharepoint
