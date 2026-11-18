# CasaSAPO for Claude

CasaSAPO helps you search property listings in Portugal and review listings returned by the CasaSAPO service. The plugin connects Claude to the official CasaSAPO remote MCP server and provides a property-search skill for interpreting requests and presenting results.

## Capabilities

Search properties for sale or rent by location and criteria, inspect a specific returned listing, contact its advertiser, and create search alerts. Contact and alert actions use your authenticated CasaSAPO account when required. Listing information is supplied by advertisers and is not independently verified by this plugin.

## Requirements

Claude must be able to reach `https://casa.sapo.pt/mcp`. Some actions require signing in to CasaSAPO and authorizing access. Availability of plugin installation and connector features depends on your Claude plan and organization settings.

## Example requests

- Find apartments for sale in Lisbon under 300,000 euros.
- Search for houses with a pool for sale in Cascais.
- Show rooms for rent in Coimbra.
- Tell me more about the first property in those results.

## Authentication and data

Search requests are sent to CasaSAPO. Contact and alert requests may send the selected listing and criteria to CasaSAPO using the account you authorize. Review the CasaSAPO terms before using these actions. Do not rely on listing information as independent verification of a property or advertiser.

## Links

- Website: <https://casa.sapo.pt>
- [Privacy policy](https://casa.sapo.pt/en-gb/privacy-policy)
- [Terms of service](https://casa.sapo.pt/en_gb/general/condicoes/portal_conditions.php)

## License

The plugin files are distributed under the proprietary license in `LICENSE`. That license does not grant rights to the CasaSAPO service or its listing data.
