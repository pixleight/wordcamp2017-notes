# But Why? 10 Use Cases for the REST API

John Eckman. Not Jon Heller, not searching for the perfect search  
@jeckman

## Headless (or head optional)

Breaking operation between the "body", the system to create and manage content — and the "head", the system that displays that content.

  - Dynamic, app-like user experience
  - Pace Layering: change front end more frequently
  - Reduce attack surface

Example: WMU.org (wamu.org?) — React.js front end, Wordpress back end.

## Multi-Headed

  - Customized experiences for different audiences
  - Single instance of content, editorial, and workflow
  - Serve clients, partners, employees, or different segments

## Infrastructure

  - Wordpress as one service among others
  - Multiple inputs & outputs
  - Likely incorporates headless/multiheaded

## In-Site Content

  - Load more ("infinite scroll")
  - Filtered/faceted search results (w/ Elastic Press)
  - Related stories/recirculation
  - Sponsored Content

## Cross-Site Content

  - Syndication push/pull across sites in a network
  - Pull based on taxonomy, post type endpoint
  - Admin experience to "push" article I am viewing to a site to which I have permissions
  - Including sites NOT on multisite / not using WP

## Improved Author Experience

  - Creating complex content types
  - Infrequent user forms & guided wizards
  - Embedding content creation in existing workflows

## Improved Editor experience

  - Replacement dashboards (à la Calypso)
  - Better management of relationships across post types
  - Sorting/Deleting/Updating in batches
  - Curation - selecting and ordering content

## Integration with Other Services

  - Email newsletter providers
  - Google Docs
  - Encapsulate outgoing calls via internal custom endpoint
  - Import from video management systems
  - Populating existing CMS (replace back-end in place)
  - Provide an API to your data for others to build on

## Integration with Mobile Apps

  - Standardized format for content pull into native app experiences
  - Bi-directional: create and update custom post types based on user actions in app
  - Future-proofing - What's behind the API could be swapped later

## Integration with Desktop Apps

  - Providing contextual, on-demand help
  - Intake of orders, requests for quotes
