# BL Command Help (Recursive)

## bl

usage: bl [OPTIONS] COMMAND

bl is a command-line interface for the BinaryLane API

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `account            Access account commands`
- `action             Access action commands`
- `configure          Configure access to BinaryLane API`
- `domain             Access domain commands`
- `image              Access image commands`
- `load-balancer      Access load-balancer commands`
- `region             Access region commands`
- `server             Access server commands`
- `size               Access size commands`
- `software           Access software commands`
- `ssh-key            Access ssh-key commands`
- `version            Show the current version`
- `vpc                Access vpc commands`


## bl account

usage: bl account [OPTIONS] COMMAND

Access account commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `balance            Fetch current balance information`
- `get                Fetch information about the current account`
- `invoice            Access account invoice commands`


## bl account balance

usage: bl account balance [OPTIONS] 

Fetch current balance information

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`


## bl account get

usage: bl account get [OPTIONS] 

Fetch information about the current account

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`


## bl account invoice

usage: bl account invoice [OPTIONS] COMMAND

Access account invoice commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `get                Fetch an invoice`
- `list               Fetch invoices`
- `overdue            Fetch unpaid failed invoices`


## bl account invoice get

usage: bl account invoice get [OPTIONS] INVOICE_ID

Fetch an invoice

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `INVOICE_ID         The ID of the invoice to fetch.`


## bl account invoice list

usage: bl account invoice list [OPTIONS] 

Fetch invoices

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "invoice_id,invoice_numb`
- `er,amount,tax,created,date_due,date_overdue,paid,refun`
- `ded")`
- `-1, --single-column   List one invoice_id per line.`

Available fields:
- `invoice_id            The ID of the invoice.`
- `invoice_number        The invoice number for this invoice.`
- `amount                The amount of the invoice in AU$.`
- `tax_code              The tax code that was applied to transactions on this`
- `invoice.`
- `tax                   The amount of tax (if any) that was charged on the`
- `transactions on this invoice.`
- `created               The date in ISO8601 format this invoice was created.`
- `date_due              The date in ISO8601 format this invoice is due for`
- `payment.`
- `date_overdue          The date in ISO8601 format this invoice is considered`
- `overdue.`
- `paid                  If this is true the invoice has been paid.`
- `refunded              If this is true the payment for this invoice has been`
- `refunded.`
- `invoice_items         The individual items that make up invoice.`
- `reference             The reference for this invoice. If this invoice is for`
- `a single service this may identify the service,`
- `otherwise it will be the account reference.`
- `payment_failure_count`
- `If this is included it indicates the number of failed`
- `attempts at processing payment for this invoice that`
- `have occurred.`
- `invoice_download_url  The download URL for the rendered version of the`
- `invoice.`


## bl account invoice overdue

usage: bl account invoice overdue [OPTIONS] 

Fetch unpaid failed invoices

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "invoice_id,invoice_numb`
- `er,amount,tax,created,date_due,date_overdue,paid,refun`
- `ded")`
- `-1, --single-column   List one invoice_id per line.`

Available fields:
- `invoice_id            The ID of the invoice.`
- `invoice_number        The invoice number for this invoice.`
- `amount                The amount of the invoice in AU$.`
- `tax_code              The tax code that was applied to transactions on this`
- `invoice.`
- `tax                   The amount of tax (if any) that was charged on the`
- `transactions on this invoice.`
- `created               The date in ISO8601 format this invoice was created.`
- `date_due              The date in ISO8601 format this invoice is due for`
- `payment.`
- `date_overdue          The date in ISO8601 format this invoice is considered`
- `overdue.`
- `paid                  If this is true the invoice has been paid.`
- `refunded              If this is true the payment for this invoice has been`
- `refunded.`
- `invoice_items         The individual items that make up invoice.`
- `reference             The reference for this invoice. If this invoice is for`
- `a single service this may identify the service,`
- `otherwise it will be the account reference.`
- `payment_failure_count`
- `If this is included it indicates the number of failed`
- `attempts at processing payment for this invoice that`
- `have occurred.`
- `invoice_download_url  The download URL for the rendered version of the`
- `invoice.`


## bl action

usage: bl action [OPTIONS] COMMAND

Access action commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `get                Fetch an existing action`
- `list               List all actions`
- `proceed            Respond to a UserInteractionRequired action`


## bl action get

usage: bl action get [OPTIONS] ACTION_ID

Fetch an existing action

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `ACTION_ID          The ID of the action to fetch.`


## bl action list

usage: bl action list [OPTIONS] 

List all actions

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "id,type,started_at,comp`
- `leted_at,resource_id,status,result_data")`
- `-1, --single-column   List one id per line.`

Available fields:
- `id                    The ID of this action.`
- `status                One of the following values:`
- `in-progress - This action is currently in progress.`
- `completed - This action has successfully completed.`
- `errored - An error was encountered while processing`
- `the action.`
- `type                  The type of this action.`
- `started_at            The timestamp in ISO8601 format of when processing of`
- `this action started.`
- `progress              Information about the current progress of the action.`
- `Some actions are divided into 'steps' and this may`
- `also contain information about the current and`
- `completed steps.`
- `completed_at          The timestamp in ISO8601 format of when processing of`
- `this action completed. If this value is null the`
- `action is currently in progress.`
- `resource_type         The resource type (if any) associated with this`
- `action.`
- `resource_id           The resource id of the resource (if any) associated`
- `with this action.`
- `region                The region (if any) of the resource associated with`
- `this action.`
- `region_slug           The region slug (if any) of the resource associated`
- `with this action.`
- `result_data           Returned information from a completed action. For`
- `example: a successful completed 'ping' action will`
- `have the ping value in ms in this field.`
- `blocking_invoice_id   If this Action is currently blocked by an invoice that`
- `requires payment this property will be set.`
- `user_interaction_required`
- `If this is not null the action is waiting on a`
- `response from the user.`


## bl action proceed

usage: bl action proceed [OPTIONS] ACTION_ID --proceed PROCEED

Respond to a UserInteractionRequired action

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `ACTION_ID             The ID of the action for which this is a response.`
- `--proceed, --no-proceed`
- `Please see the documentation for each type of`
- `interaction for the effect of providing 'true' or`
- `'false' here.`


## bl configure

usage: bl configure [OPTIONS] 

Configure access to BinaryLane API

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`


## bl domain

usage: bl domain [OPTIONS] COMMAND

Access domain commands

Options:
- `--help                Display available commands and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`

Available Commands:
- `create                Create a new domain`
- `delete                Delete an existing domain`
- `get                   Fetch an existing domain`
- `list                  List all domains`
- `nameservers           Access domain nameservers commands`
- `record                Access domain record commands`
- `refresh-nameserver-cache`
- `Refresh cached nameserver domain records`


## bl domain create

usage: bl domain create [OPTIONS] --name NAME [PARAMETERS]

Create a new domain

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `--name NAME           The domain name to add to the DNS management system.`

Parameters:
- `--ip-address IP_ADDRESS`
- `An optional IPv4 address that will be used to create`
- `an A record for the root domain.`


## bl domain delete

usage: bl domain delete [OPTIONS] DOMAIN_NAME

Delete an existing domain

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `DOMAIN_NAME        The name of the domain to delete.`


## bl domain get

usage: bl domain get [OPTIONS] DOMAIN_NAME

Fetch an existing domain

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `DOMAIN_NAME        The name of the domain to fetch.`


## bl domain list

usage: bl domain list [OPTIONS] 

List all domains

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...   Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "name,zone_file")`
- `-1, --single-column  List one name per line.`

Available fields:
- `name                 The name of the domain.`
- `current_nameservers  The current authoritative name servers for this domain.`
- `zone_file            The zone file for the selected domain. If the DNS`
- `records for this domain are not managed locally this is`
- `what the zone file would be if the authority was`
- `delegated to us.`
- `ttl                  The time to live for records in this domain in seconds.`
- `If the DNS records for this domain are not managed`
- `locally this will be what the TTL would be if the`
- `authority was delegated to us.`


## bl domain nameservers

usage: bl domain nameservers [OPTIONS] COMMAND

Access domain nameservers commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `list               List all public nameservers`


## bl domain nameservers list

usage: bl domain nameservers list [OPTIONS] 

List all public nameservers

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`


## bl domain record

usage: bl domain record [OPTIONS] COMMAND

Access domain record commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `create             Create a new domain record`
- `delete             Delete an existing domain record`
- `get                Fetch an existing domain record`
- `list               List all domain records for a domain`
- `update             Update an existing domain record`


## bl domain record create

usage: bl domain record create [OPTIONS] DOMAIN_NAME [PARAMETERS]

Create a new domain record

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `DOMAIN_NAME          The domain name for which the record should be created.`

Parameters:
- `--type TYPE          The type of the DNS record. (One of: A, AAAA, CAA,`
- `CNAME, MX, NS, SOA, SRV, TXT)`
- `--name NAME          The subdomain for this record. Use @ for records on the`
- `domain itself, and * to create a wildcard record.`
- `--data DATA          A general data field that has different functions`
- `depending on the record type.`
- `--priority PRIORITY  A priority value that is only relevant for SRV and MX`
- `records.`
- `--port PORT          A port value that is only relevant for SRV records.`
- `--ttl TTL            This value is the time to live for the record, in`
- `seconds.`
- `--weight WEIGHT      The weight value that is only relevant for SRV records.`
- `--flags FLAGS        An unsigned integer between 0-255 that is only relevant`
- `for CAA records.`
- `--tag TAG            A parameter tag that is only relevant for CAA records.`


## bl domain record delete

usage: bl domain record delete [OPTIONS] DOMAIN_NAME RECORD_ID

Delete an existing domain record

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `DOMAIN_NAME        The domain name for which the record should be deleted.`
- `RECORD_ID          The ID of the record to delete.`


## bl domain record get

usage: bl domain record get [OPTIONS] DOMAIN_NAME RECORD_ID

Fetch an existing domain record

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `DOMAIN_NAME        The domain name for which the record should be fetched.`
- `RECORD_ID          The ID of the record to fetch.`


## bl domain record list

usage: bl domain record list [OPTIONS] DOMAIN_NAME [PARAMETERS]

List all domain records for a domain

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...   Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "id,name,type,data")`
- `-1, --single-column  List one id per line.`

Arguments:
- `DOMAIN_NAME          The domain name for which records should be listed.`

Parameters:
- `--type TYPE          | Value | Description |`
- `| ----- | ----------- |`
- `| A | Map an IPv4 address to a hostname. |`
- `| AAAA | Map an IPv6 address to a hostname. |`
- `| CAA | Restrict which certificate authorities are`
- `permitted to issue certificates for a domain. |`
- `| CNAME | Define an alias for your canonical hostname.`
- `|`
- `| MX | Define the mail exchanges that handle mail for`
- `the domain. |`
- `| NS | Define the nameservers that manage the domain. |`
- `| SOA | The Start of Authority record for the zone. |`
- `| SRV | Specify a server by hostname and port to handle`
- `a service or services. |`
- `| TXT | Define a string of text that is associated with`
- `a hostname. |`
- `(One of: A, AAAA, CAA, CNAME, MX, NS, SOA, SRV, TXT)`
- `--name NAME          Only return records for this subdomain name.`

Available fields:
- `id                   The ID of this domain record.`
- `type                 A general data field that has different functions`
- `depending on the record type.`
- `| Value | Description |`
- `| ----- | ----------- |`
- `| A | Map an IPv4 address to a hostname. |`
- `| AAAA | Map an IPv6 address to a hostname. |`
- `| CAA | Restrict which certificate authorities are`
- `permitted to issue certificates for a domain. |`
- `| CNAME | Define an alias for your canonical hostname.`
- `|`
- `| MX | Define the mail exchanges that handle mail for`
- `the domain. |`
- `| NS | Define the nameservers that manage the domain. |`
- `| SOA | The Start of Authority record for the zone. |`
- `| SRV | Specify a server by hostname and port to handle`
- `a service or services. |`
- `| TXT | Define a string of text that is associated with`
- `a hostname. |`
- `name                 The subdomain, alias, or service defined by the record.`
- `ttl                  This value is the time to live for the record in`
- `seconds.`
- `data                 Variable data depending on record type.`
- `priority             A priority value that is only relevant for SRV and MX`
- `records.`
- `port                 A port value that is only relevant for SRV records.`
- `weight               The weight value that is only relevant for SRV records.`
- `flags                An unsigned integer between 0-255 that is only relevant`
- `for CAA records.`
- `tag                  A parameter tag that is only relevant for CAA records.`


## bl domain record update

usage: bl domain record update [OPTIONS] DOMAIN_NAME RECORD_ID [PARAMETERS]

Update an existing domain record

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `DOMAIN_NAME          The domain name for which the record should be updated.`
- `RECORD_ID            The ID of the record to update.`

Parameters:
- `--type TYPE          The type of the DNS record. (One of: A, AAAA, CAA,`
- `CNAME, MX, NS, SOA, SRV, TXT)`
- `--name NAME          The subdomain for this record. Use @ for records on the`
- `domain itself, and * to create a wildcard record.`
- `--data DATA          A general data field that has different functions`
- `depending on the record type.`
- `--priority PRIORITY  A priority value that is only relevant for SRV and MX`
- `records.`
- `--port PORT          A port value that is only relevant for SRV records.`
- `--ttl TTL            This value is the time to live for the record, in`
- `seconds.`
- `--weight WEIGHT      The weight value that is only relevant for SRV records.`
- `--flags FLAGS        An unsigned integer between 0-255 that is only relevant`
- `for CAA records.`
- `--tag TAG            A parameter tag that is only relevant for CAA records.`


## bl domain refresh-nameserver-cache

usage: bl domain refresh-nameserver-cache [OPTIONS] 

Refresh cached nameserver domain records

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`


## bl domain Refresh

Command '['bl', 'domain', 'Refresh', '--help']' returned non-zero exit status 2.

## bl image

usage: bl image [OPTIONS] COMMAND

Access image commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `download           Download an existing image`
- `get                Fetch an existing image`
- `list               List all images`
- `update             Update an existing image`


## bl image download

usage: bl image download [OPTIONS] IMAGE_ID

Download an existing image

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `IMAGE_ID           The ID of the image to download.`


## bl image get

usage: bl image get [OPTIONS] IMAGE_ID_OR_SLUG

Fetch an existing image

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `IMAGE_ID_OR_SLUG   The ID or Slug (if an operating system) of the image to`
- `retrieve.`


## bl image list

usage: bl image list [OPTIONS] [PARAMETERS]

List all images

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default:`
- `"id,slug,distribution,name")`
- `-1, --single-column   List one id per line.`

Parameters:
- `--type TYPE           Queries for distribution will include images that have`
- `pre-installed applications. (One of: distribution,`
- `backup)`
- `--private, --no-private`
- `Provide 'true' to only list private images. 'false'`
- `has no effect.`

Available fields:
- `id                    The ID of this image.`
- `name                  If this is an operating system image, this is the name`
- `of the operating system version. If this is a backup`
- `image, this is the label of the backup if it exists,`
- `otherwise it is the UTC timestamp of the creation of`
- `the image.`
- `type                  One of the following values:`
- `custom - An image uploaded by a user.`
- `snapshot - A snapshot. Snapshot creation is not`
- `currently supported so only distribution images will`
- `have this value.`
- `backup - A backup of a server.`
- `public                A public image is available to all users. A private`
- `image is available only to the account that created`
- `the image.`
- `regions               The slugs of the regions where the image is available`
- `for use.`
- `min_disk_size         For a distribution image this is the minimum disk size`
- `in GB required to install the operating system. For a`
- `backup image this is the minimum total disk size in GB`
- `required to restore the backup.`
- `size_gigabytes        For a distribution image this is the disk size used in`
- `GB by the operating system on initial install. For a`
- `backup image this is the size of the compressed backup`
- `image in GB.`
- `status                One of the following values:`
- `NEW - The image is new.`
- `available - The image is available for use.`
- `pending - The image is pending and is not yet`
- `available for use.`
- `deleted - The image has been deleted and is no`
- `longer available for use.`
- `distribution_info     This object may provide further information about the`
- `distribution.`
- `distribution          If this is an operating system image, this is the name`
- `of the distribution. If this is a backup image, this`
- `is the name of the distribution the server is using.`
- `full_name             If this is an operating system image, this is the name`
- `and version of the distribution. If this is a backup`
- `image, this is the server hostname and label of the`
- `backup if it exists, otherwise it is the server`
- `hostname and UTC timestamp of the creation of the`
- `image.`
- `slug                  If this is an operating system image this is a slug`
- `which may be used as an alternative to the ID as a`
- `reference.`
- `created_at            If this is a backup image this is the date and time in`
- `ISO8601 format when the image was created.`
- `description           A description that may provide further details or`
- `warnings about the image.`
- `error_message         If the image creation failed this may provide further`
- `information.`
- `min_memory_megabytes  This is minimum memory in MB necessary to support this`
- `operating system (or the base operating system for a`
- `backup image).`
- `distribution_surcharges`
- `If this is not null the use of this image may incur`
- `surcharges above the base cost of the server. All`
- `costs are in AU$.`
- `backup_info           If this image is a backup, this object will provide`
- `further information.`


## bl image update

usage: bl image update [OPTIONS] IMAGE_ID [PARAMETERS]

Update an existing image

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `IMAGE_ID              The ID of the image to update.`

Parameters:
- `--name NAME           Optional: a new display name for this image. Do not`
- `provide to leave the display name unchanged, submit an`
- `empty string to clear the display name.`
- `--locked, --no-locked`
- `Optional: you may choose to lock an individual backup`
- `in which case we will not update that backup until you`
- `unlock it. Do not provide to leave the locked status`
- `unchanged.`


## bl load-balancer

usage: bl load-balancer [OPTIONS] COMMAND

Access load-balancer commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `availability       Fetch load balancer availability and pricing`
- `create             Create a new load balancer`
- `delete             Cancel an existing load balancer`
- `get                Fetch an existing load balancer`
- `list               List all load balancers`
- `rule               Access load-balancer rule commands`
- `server             Access load-balancer server commands`
- `update             Update an existing load balancer`


## bl load-balancer availability

usage: bl load-balancer availability [OPTIONS] 

Fetch load balancer availability and pricing

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...   Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default:`
- `"anycast,price_monthly,price_hourly")`
- `-1, --single-column  List one anycast per line.`

Available fields:
- `anycast              If true this is an Anycast load balancer option.`
- `price_monthly        Monthly Price in AU$.`
- `price_hourly         Hourly price in AU$.`
- `regions              The slugs of regions where this load balancer option is`
- `available. If this is an Anycast load balancer option`
- `this will be null.`


## bl load-balancer create

usage: bl load-balancer create [OPTIONS] --name NAME [PARAMETERS] [+rule ... ]

Create a new load balancer

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `--name NAME           The hostname of the load balancer.`

Parameters:
- `--server-ids [SERVER_IDS ...]`
- `A list of server IDs to assign to this load balancer.`
- `--region REGION       Leave null to create an anycast load balancer.`

Forwarding Rules:
- `The rules that control which traffic the load balancer will forward to`
- `servers in the pool. Leave null to accept a default "HTTP" only forwarding`
- `rule.`

- `+rule                 Required marker at start of each item.`
- `--entry-protocol ENTRY_PROTOCOL`
- `The protocol that traffic must match for this load`
- `balancer to forward traffic according to this rule.`

Health Check:
- `The rules that determine which servers are considered 'healthy' and in the`
- `server pool for the load balancer. Leave this null to accept appropriate`
- `defaults based on the forwarding_rules.`

- `--protocol PROTOCOL   Leave null to accept the default HTTP protocol. (One`
- `of: http, https, both)`
- `--path PATH           Leave null to accept the default '/' path.`


## bl load-balancer delete

usage: bl load-balancer delete [OPTIONS] LOAD_BALANCER_ID

Cancel an existing load balancer

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `LOAD_BALANCER_ID   The ID of the load balancer to cancel.`


## bl load-balancer get

usage: bl load-balancer get [OPTIONS] LOAD_BALANCER_ID

Fetch an existing load balancer

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `LOAD_BALANCER_ID   The ID of the load balancer to fetch.`


## bl load-balancer list

usage: bl load-balancer list [OPTIONS] 

List all load balancers

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...   Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "id,name,region,ip")`
- `-1, --single-column  List one id per line.`

Available fields:
- `id                   The ID of the load balancer.`
- `name                 The hostname of the load balancer.`
- `ip                   The IPv4 address of the load balancer.`
- `status               One of the following values:`
- `new - The load balancer is currently being built and`
- `is not ready to accept connections.`
- `active - The load balancer is available.`
- `errored - The load balancer is in an errored state.`
- `created_at           The date and time in ISO8601 format of the creation of`
- `the load balancer.`
- `forwarding_rules     The rules that control which traffic the load balancer`
- `will forward to servers in the pool.`
- `health_check         The rules that determine which servers are considered`
- `'healthy' and in the server pool for the load balancer.`
- `server_ids           The server IDs of the servers that are currently in the`
- `load balancer pool (regardless of their current`
- `'health').`
- `region               The region the load balancer is located in. If this`
- `value is null the load balancer is an 'AnyCast' load`
- `balancer.`


## bl load-balancer rule

usage: bl load-balancer rule [OPTIONS] COMMAND

Access load-balancer rule commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `create             Add forwarding rules to an existing load balancer`
- `delete             Remove forwarding rules from an existing load balancer`


## bl load-balancer rule create

usage: bl load-balancer rule create [OPTIONS] LOAD_BALANCER_ID [+rule ... ]

Add forwarding rules to an existing load balancer

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `LOAD_BALANCER_ID      The ID of the load balancer to which forwarding rules`
- `should be added.`

Forwarding Rules:
- `The rules that control which traffic the load balancer will forward to`
- `servers in the pool.`

- `+rule                 Required marker at start of each item.`
- `--entry-protocol ENTRY_PROTOCOL`
- `The protocol that traffic must match for this load`
- `balancer to forward traffic according to this rule.`


## bl load-balancer rule delete

usage: bl load-balancer rule delete [OPTIONS] LOAD_BALANCER_ID [+rule ... ]

Remove forwarding rules from an existing load balancer

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `LOAD_BALANCER_ID      The ID of the load balancer for which forwarding rules`
- `should be removed.`

Forwarding Rules:
- `The rules that control which traffic the load balancer will forward to`
- `servers in the pool.`

- `+rule                 Required marker at start of each item.`
- `--entry-protocol ENTRY_PROTOCOL`
- `The protocol that traffic must match for this load`
- `balancer to forward traffic according to this rule.`


## bl load-balancer server

usage: bl load-balancer server [OPTIONS] COMMAND

Access load-balancer server commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `create             Add servers to an existing load balancer`
- `delete             Remove servers from an existing load balancer`


## bl load-balancer server create

usage: bl load-balancer server create [OPTIONS] LOAD_BALANCER_ID --server-ids SERVER_IDS

Add servers to an existing load balancer

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `LOAD_BALANCER_ID      The ID of the load balancer to which servers should be`
- `added.`
- `--server-ids [SERVER_IDS ...]`
- `A list of server IDs.`


## bl load-balancer server delete

usage: bl load-balancer server delete [OPTIONS] LOAD_BALANCER_ID --server-ids SERVER_IDS

Remove servers from an existing load balancer

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `LOAD_BALANCER_ID      The ID of the load balancer for which servers should`
- `be removed.`
- `--server-ids [SERVER_IDS ...]`
- `A list of server IDs.`


## bl load-balancer update

usage: bl load-balancer update [OPTIONS] LOAD_BALANCER_ID --name NAME [PARAMETERS] [+rule ... ]

Update an existing load balancer

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `LOAD_BALANCER_ID      The ID of the load balancer to update.`
- `--name NAME           The hostname of the load balancer.`

Parameters:
- `--server-ids [SERVER_IDS ...]`
- `A list of server IDs to assign to this load balancer.`

Forwarding Rules:
- `The rules that control which traffic the load balancer will forward to`
- `servers in the pool. Leave null to accept a default "HTTP" only forwarding`
- `rule.`

- `+rule                 Required marker at start of each item.`
- `--entry-protocol ENTRY_PROTOCOL`
- `The protocol that traffic must match for this load`
- `balancer to forward traffic according to this rule.`

Health Check:
- `The rules that determine which servers are considered 'healthy' and in the`
- `server pool for the load balancer. Leave this null to accept appropriate`
- `defaults based on the forwarding_rules.`

- `--protocol PROTOCOL   Leave null to accept the default HTTP protocol. (One`
- `of: http, https, both)`
- `--path PATH           Leave null to accept the default '/' path.`


## bl region

usage: bl region [OPTIONS] COMMAND

Access region commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `list               List all regions`


## bl region list

usage: bl region list [OPTIONS] 

List all regions

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...   Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "slug,name")`
- `-1, --single-column  List one slug per line.`

Available fields:
- `slug                 The unique slug for this region.`
- `name                 The name of this region.`
- `sizes                The slugs of the sizes available in this region.`
- `available            Whether this region is available for the allocation of`
- `new resources.`
- `features             A list of features available for resources in this`
- `region.`
- `name_servers         A list of nameservers available for resources in this`
- `region.`


## bl server

usage: bl server [OPTIONS] COMMAND

Access server commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `action             Access server action commands`
- `alert              Access server alert commands`
- `backup             Access server backup commands`
- `console            Fetch the console URLs for a server`
- `create             Create a new server`
- `data-usage         Access server data-usage commands`
- `delete             Cancel an existing server`
- `failover-ip        Access server failover-ip commands`
- `feature            Access server feature commands`
- `firewall           Access server firewall commands`
- `get                Fetch an existing server`
- `ipv6-ptr-ns        Access server ipv6-ptr-ns commands`
- `kernel             Access server kernel commands`
- `list               List all servers`
- `metrics            Access server metrics commands`
- `snapshot           Access server snapshot commands`
- `software           List all enabled software for a server`
- `user-data          Fetch the currently set UserData for a server`


## bl server action

usage: bl server action [OPTIONS] COMMAND

Access server action commands

Options:
- `--help                Display available commands and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`

Available Commands:
- `add-disk              Create an additional disk for a server`
- `attach-backup         Attach a backup to a server`
- `change-advanced-features`
- `Change the advanced features of a server`
- `change-advanced-firewall-rules`
- `Change the advanced firewall rules for a server`
- `change-backup-schedule`
- `Change the backup schedule of a server`
- `change-ipv6           Enable or disable IPv6 for a server`
- `change-ipv6-reverse-nameservers`
- `Update the IPv6 reverse name servers for a server`
- `change-kernel         Change the kernel of a server`
- `change-manage-offsite-backup-copies`
- `Change the management of offsite backup copies`
- `change-network        Move a server to an existing network`
- `change-offsite-backup-location`
- `Change the offsite backup location of a server`
- `change-partner        Add, update or remove a partner server for a server`
- `change-port-blocking  Change the port blocking for a server`
- `change-reverse-name   Change the reverse name for an IPv4 address on a`
- `server`
- `change-separate-private-network-interface`
- `Enable or disable a separate private network interface`
- `for a server in a VPC`
- `change-source-and-destination-check`
- `Enable or disable network source and destination`
- `checks for a server in a VPC`
- `change-threshold-alerts`
- `Set or update the threshold alerts for a server`
- `change-vpc-ipv4       Change the IPv4 address for a server in a VPC`
- `clone-using-backup    Restore a backup of a server to a different existing`
- `server`
- `delete-disk           Delete an additional disk for a server`
- `detach-backup         Detach any attached backup from a server`
- `disable-backups       Disable backups for an existing server`
- `disable-selinux       Disable SE linux for a server`
- `enable-backups        Enable two daily backups for an existing server`
- `enable-ipv6           Enable IPv6 for a server`
- `get                   Fetch an action for a server`
- `is-running            Check if a server is running`
- `list                  List all actions for a server`
- `password-reset        Reset the password of a server`
- `ping                  Attempt to ping a server`
- `power-cycle           Power a server off and then on`
- `power-off             Power a server off`
- `power-on              Power a server on`
- `reboot                Request a server perform a reboot`
- `rebuild               Rebuild an existing server`
- `rename                Rename a server`
- `resize                Update the size and related options for a server`
- `resize-disk           Alter the size of an existing disk for a server`
- `restore               Restore a backup to a server`
- `shutdown              Request a server perform a shutdown`
- `take-backup           Take a backup of a server`
- `uncancel              Revert the cancellation of a server`
- `uptime                Check the uptime of a server`


## bl server action add-disk

usage: bl server action add-disk [OPTIONS] SERVER --size-gigabytes SIZE_GIGABYTES [PARAMETERS]

Create an additional disk for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--size-gigabytes SIZE_GIGABYTES`
- `The size of the new disk in GB. The server must have`
- `at least this much unallocated storage space.`

Parameters:
- `--description DESCRIPTION`
- `An optional description for the disk. If this is null`
- `a default description will be added. Submit an empty`
- `string to prevent the default description being added.`


## bl server action attach-backup

usage: bl server action attach-backup [OPTIONS] SERVER --image IMAGE

Attach a backup to a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`
- `--image IMAGE      Only attaching backup images is currently supported.`


## bl server action change-advanced-features

usage: bl server action change-advanced-features [OPTIONS] SERVER [PARAMETERS]

Change the advanced features of a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`

Parameters:
- `--enabled-advanced-features [ENABLED_ADVANCED_FEATURES ...]`
- `Do not provide or set to null to keep existing`
- `advanced features. Provide an empty array to disable`
- `all advanced features, otherwise provide an array with`
- `selected advanced features. If provided, any currently`
- `enabled advanced features that aren't included will be`
- `disabled. (One of: emulated-hyperv, emulated-devices,`
- `nested-virt, driver-disk, unset-uuid, local-rtc,`
- `emulated-tpm, cloud-init, qemu-guest-agent, uefi-boot)`
- `--processor-model PROCESSOR_MODEL`
- `Do not provide or set to null to keep existing`
- `processor model.`
- `--automatic-processor-model, --no-automatic-processor-model`
- `Set to true to use best available processor model. If`
- `this is provided the processor_model property must not`
- `be provided.`
- `--machine-type MACHINE_TYPE`
- `Do not provide or set to null to keep existing machine`
- `type. (One of: pc_i440fx_1point5, pc_i440fx_2point11,`
- `pc_i440fx_4point1, pc_i440fx_4point2,`
- `pc_i440fx_5point0, pc_i440fx_5point1)`
- `--automatic-machine-type, --no-automatic-machine-type`
- `Set to true to use best available machine type. If`
- `this is provided the machine_type property must not be`
- `provided.`
- `--video-device VIDEO_DEVICE`
- `Do not provide or set to null to keep existing video`
- `device. (One of: cirrus-logic, standard, virtio,`
- `virtio-wide)`


## bl server action Change

Command '['bl', 'server', 'action', 'Change', '--help']' returned non-zero exit status 2.

## bl server action change-advanced-firewall-rules

usage: bl server action change-advanced-firewall-rules [OPTIONS] SERVER [+rule ... ]

Change the advanced firewall rules for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`

Firewall Rules:
- `A list of rules for the server. NB: that any existing rules that are not`
- `included will be removed. Submit an empty list to clear all rules.`

- `+rule                 Required marker at start of each item.`
- `--source-addresses SOURCE_ADDRESSES`
- `The source addresses to match for this rule. Each`
- `address may be an individual IPv4 address or a range`
- `in IPv4 CIDR notation.`
- `--destination-addresses DESTINATION_ADDRESSES`
- `The destination addresses to match for this rule. Each`
- `address may be an individual IPv4 address or a range`
- `in IPv4 CIDR notation.`
- `--protocol PROTOCOL   The protocol to match for this rule.`
- `--action ACTION       The action to take when there is a match on this rule.`
- `--destination-ports DESTINATION_PORTS`
- `The destination ports to match for this rule. Leave`
- `null or empty to match on all ports.`
- `--description DESCRIPTION`
- `A description to assist in identifying this rule.`
- `Commonly used to record the reason for the rule or the`
- `intent behind it, e.g. "Block access to RDP" or "Allow`
- `access from HQ".`


## bl server action Change

Command '['bl', 'server', 'action', 'Change', '--help']' returned non-zero exit status 2.

## bl server action change-backup-schedule

usage: bl server action change-backup-schedule [OPTIONS] SERVER [PARAMETERS]

Change the backup schedule of a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`

Parameters:
- `--backup-hour-of-day BACKUP_HOUR_OF_DAY`
- `Do not provide a value to keep the current setting.`
- `--backup-day-of-week BACKUP_DAY_OF_WEEK`
- `Sunday is 0, Monday is 1 etc. Do not provide a value`
- `to keep the current setting.`
- `--backup-day-of-month BACKUP_DAY_OF_MONTH`
- `Do not provide a value to keep the current setting.`


## bl server action Change

Command '['bl', 'server', 'action', 'Change', '--help']' returned non-zero exit status 2.

## bl server action change-ipv6

usage: bl server action change-ipv6 [OPTIONS] SERVER --enabled ENABLED

Enable or disable IPv6 for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--enabled, --no-enabled`
- `The desired enabled status of IPv6.`


## bl server action change-ipv6-reverse-nameservers

usage: bl server action change-ipv6-reverse-nameservers [OPTIONS] SERVER --ipv6-reverse-nameservers IPV6_REVERSE_NAMESERVERS

Update the IPv6 reverse name servers for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--ipv6-reverse-nameservers [IPV6_REVERSE_NAMESERVERS ...]`
- `A list of all IPv6 reverse name servers for this`
- `server. Any existing reverse name servers that are`
- `omitted from the list will be removed from the server.`


## bl server action Update

Command '['bl', 'server', 'action', 'Update', '--help']' returned non-zero exit status 2.

## bl server action change-kernel

usage: bl server action change-kernel [OPTIONS] SERVER --kernel KERNEL

Change the kernel of a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`
- `--kernel KERNEL    The ID of the kernel to use.`


## bl server action change-manage-offsite-backup-copies

usage: bl server action change-manage-offsite-backup-copies [OPTIONS] SERVER --manage-offsite-backup-copies MANAGE_OFFSITE_BACKUP_COPIES

Change the management of offsite backup copies

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--manage-offsite-backup-copies, --no-manage-offsite-backup-copies`
- `This only has effect if a custom offsite location is`
- `being used: the internal offsite backup location`
- `always manages copies. If this is true old offsite`
- `backups will be removed once the replacement upload is`
- `complete. If this is false backups must be removed`
- `from the Amazon S3 bucket manually. Amazon will charge`
- `your S3 account at their standard rate for every`
- `backup stored.`


## bl server action Change

Command '['bl', 'server', 'action', 'Change', '--help']' returned non-zero exit status 2.

## bl server action change-network

usage: bl server action change-network [OPTIONS] SERVER [PARAMETERS]

Move a server to an existing network

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`

Parameters:
- `--vpc-id VPC_ID    If this is null the server will be moved into the default`
- `public network for the server's region.`


## bl server action change-offsite-backup-location

usage: bl server action change-offsite-backup-location [OPTIONS] SERVER [PARAMETERS]

Change the offsite backup location of a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`

Parameters:
- `--offsite-backup-location OFFSITE_BACKUP_LOCATION`
- `Do not provide or set to null to use the internal`
- `offsite backup location, otherwise this must be a`
- `valid Amazon S3 bucket address. If this is provided`
- `Amazon will charge your S3 account at their standard`
- `rate for every backup stored.`


## bl server action Change

Command '['bl', 'server', 'action', 'Change', '--help']' returned non-zero exit status 2.

## bl server action change-partner

usage: bl server action change-partner [OPTIONS] SERVER [PARAMETERS]

Add, update or remove a partner server for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`

Parameters:
- `--partner-server-id PARTNER_SERVER_ID`
- `Leave this null to remove the server partnership. The`
- `partner server must be in the same region as the`
- `target server.`


## bl server action change-port-blocking

usage: bl server action change-port-blocking [OPTIONS] SERVER --enabled ENABLED

Change the port blocking for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--enabled, --no-enabled`
- `The desired enabled status for port blocking.`


## bl server action change-reverse-name

usage: bl server action change-reverse-name [OPTIONS] SERVER --ipv4-address IPV4_ADDRESS [PARAMETERS]

Change the reverse name for an IPv4 address on a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--ipv4-address IPV4_ADDRESS`
- `The IPv4 address to set or clear the reverse name for.`

Parameters:
- `--reverse-name REVERSE_NAME`
- `Leave this null to clear the custom reverse name.`


## bl server action server

Command '['bl', 'server', 'action', 'server', '--help']' returned non-zero exit status 2.

## bl server action change-separate-private-network-interface

usage: bl server action change-separate-private-network-interface [OPTIONS] SERVER --enabled ENABLED

Enable or disable a separate private network interface for a server in a VPC

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--enabled, --no-enabled`
- `The desired enabled status of the separate second`
- `network interface.`


## bl server action Enable

Command '['bl', 'server', 'action', 'Enable', '--help']' returned non-zero exit status 2.

## bl server action for

Command '['bl', 'server', 'action', 'for', '--help']' returned non-zero exit status 2.

## bl server action change-source-and-destination-check

usage: bl server action change-source-and-destination-check [OPTIONS] SERVER --enabled ENABLED

Enable or disable network source and destination checks for a server in a VPC

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--enabled, --no-enabled`
- `The desired enabled status of the source and`
- `destination checks for network packets.`


## bl server action Enable

Command '['bl', 'server', 'action', 'Enable', '--help']' returned non-zero exit status 2.

## bl server action checks

Command '['bl', 'server', 'action', 'checks', '--help']' returned non-zero exit status 2.

## bl server action change-threshold-alerts

Command '['bl', 'server', 'action', 'change-threshold-alerts', '--help']' returned non-zero exit status 4294967295.

## bl server action Set

Command '['bl', 'server', 'action', 'Set', '--help']' returned non-zero exit status 2.

## bl server action change-vpc-ipv4

usage: bl server action change-vpc-ipv4 [OPTIONS] SERVER --current-ipv4-address CURRENT_IPV4_ADDRESS --new-ipv4-address NEW_IPV4_ADDRESS

Change the IPv4 address for a server in a VPC

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--current-ipv4-address CURRENT_IPV4_ADDRESS`
- `The existing Ipv4 address for the private VPC network`
- `adapter you wish to change.`
- `--new-ipv4-address NEW_IPV4_ADDRESS`
- `The new Ipv4 address for the private VPC network`
- `adapter.`


## bl server action clone-using-backup

usage: bl server action clone-using-backup [OPTIONS] SERVER --image-id IMAGE_ID --target-server-id TARGET_SERVER_ID [PARAMETERS]

Restore a backup of a server to a different existing server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--image-id IMAGE_ID   The ID of the image to clone. Only backup type images`
- `are currently supported. This must be a backup of the`
- `server ID in the action endpoint URL.`
- `--target-server-id TARGET_SERVER_ID`
- `The target server ID. This server's current disks will`
- `be wiped and replaced with the selected backup image.`

Parameters:
- `--name NAME           The new hostname for the target server. If this is not`
- `supplied the target server's existing hostname will be`
- `used.`


## bl server action server

Command '['bl', 'server', 'action', 'server', '--help']' returned non-zero exit status 2.

## bl server action delete-disk

usage: bl server action delete-disk [OPTIONS] SERVER --disk-id DISK_ID

Delete an additional disk for a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`
- `--disk-id DISK_ID  The ID of the existing disk. See server.disks for a list`
- `of IDs.`


## bl server action detach-backup

usage: bl server action detach-backup [OPTIONS] SERVER

Detach any attached backup from a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action disable-backups

usage: bl server action disable-backups [OPTIONS] SERVER

Disable backups for an existing server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action disable-selinux

usage: bl server action disable-selinux [OPTIONS] SERVER

Disable SE linux for a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action enable-backups

usage: bl server action enable-backups [OPTIONS] SERVER

Enable two daily backups for an existing server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action enable-ipv6

usage: bl server action enable-ipv6 [OPTIONS] SERVER

Enable IPv6 for a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action get

usage: bl server action get [OPTIONS] SERVER ACTION_ID

Fetch an action for a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `SERVER             The ID or name of the server for which the action should`
- `be fetched.`
- `ACTION_ID          The ID of the action to fetch.`


## bl server action is-running

usage: bl server action is-running [OPTIONS] SERVER

Check if a server is running

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action list

usage: bl server action list [OPTIONS] SERVER

List all actions for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "id,type,started_at,comp`
- `leted_at,resource_id,status,result_data")`
- `-1, --single-column   List one id per line.`

Arguments:
- `SERVER                The ID or name of the server for which actions should`
- `be listed.`

Available fields:
- `id                    The ID of this action.`
- `status                One of the following values:`
- `in-progress - This action is currently in progress.`
- `completed - This action has successfully completed.`
- `errored - An error was encountered while processing`
- `the action.`
- `type                  The type of this action.`
- `started_at            The timestamp in ISO8601 format of when processing of`
- `this action started.`
- `progress              Information about the current progress of the action.`
- `Some actions are divided into 'steps' and this may`
- `also contain information about the current and`
- `completed steps.`
- `completed_at          The timestamp in ISO8601 format of when processing of`
- `this action completed. If this value is null the`
- `action is currently in progress.`
- `resource_type         The resource type (if any) associated with this`
- `action.`
- `resource_id           The resource id of the resource (if any) associated`
- `with this action.`
- `region                The region (if any) of the resource associated with`
- `this action.`
- `region_slug           The region slug (if any) of the resource associated`
- `with this action.`
- `result_data           Returned information from a completed action. For`
- `example: a successful completed 'ping' action will`
- `have the ping value in ms in this field.`
- `blocking_invoice_id   If this Action is currently blocked by an invoice that`
- `requires payment this property will be set.`
- `user_interaction_required`
- `If this is not null the action is waiting on a`
- `response from the user.`


## bl server action password-reset

usage: bl server action password-reset [OPTIONS] SERVER [PARAMETERS]

Reset the password of a server

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async              Do not wait for requested action to complete`
- `--quiet              Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER               The ID or name of the server on which the action should`
- `be performed.`

Parameters:
- `--username USERNAME  The username of the user to change the password.`
- `--password PASSWORD  If this is provided the specified or default remote`
- `user's account password will be set to this value.`


## bl server action ping

usage: bl server action ping [OPTIONS] SERVER

Attempt to ping a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action power-cycle

usage: bl server action power-cycle [OPTIONS] SERVER

Power a server off and then on

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action power-off

usage: bl server action power-off [OPTIONS] SERVER

Power a server off

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action power-on

usage: bl server action power-on [OPTIONS] SERVER

Power a server on

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action reboot

usage: bl server action reboot [OPTIONS] SERVER

Request a server perform a reboot

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action rebuild

usage: bl server action rebuild [OPTIONS] SERVER [PARAMETERS]

Rebuild an existing server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`

Parameters:
- `--image IMAGE         The Operating System ID or slug or Backup image ID to`
- `use as a base for the rebuild.`
- `--name NAME           The hostname for the server. Leave null to accept the`
- `auto-generated permalink.`
- `--ssh-keys [SSH_KEYS ...]`
- `This may be either the existing SSH Keys IDs or`
- `fingerprints.`
- `--user-data USER_DATA`
- `If provided this will be used to initialise the new`
- `server. This must be left null if the Image does not`
- `support UserData, see DistributionInfo.Features for`
- `more information.`
- `--password PASSWORD   If this is provided the default remote user account's`
- `password will be set to this value. If this is null a`
- `random password will be generated and emailed to the`
- `account email address.`


## bl server action rename

usage: bl server action rename [OPTIONS] SERVER --name NAME

Rename a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`
- `--name NAME        The new hostname of your server, such as`
- `vps01.yourcompany.com.`


## bl server action resize

usage: bl server action resize [OPTIONS] SERVER [PARAMETERS] [+license ... ]

Update the size and related options for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`

Parameters:
- `--size SIZE           The slug of the selected size. Do not provide to keep`
- `the current size.`
- `--daily-backups DAILY_BACKUPS`
- `Leave null to accept the default for the size if this`
- `is a new server or to keep the current value if this`
- `is a resize of an existing server.`
- `--weekly-backups WEEKLY_BACKUPS`
- `Leave null to accept the default for the size if this`
- `is a new server or to keep the current value if this`
- `is a resize of an existing server.`
- `--monthly-backups MONTHLY_BACKUPS`
- `Leave null to accept the default for the size if this`
- `is a new server or to keep the current value if this`
- `is a resize of an existing server.`
- `--offsite-backups, --no-offsite-backups`
- `Leave null to accept the default for the size if this`
- `is a new server or to keep the current value if this`
- `is a resize of an existing server.`
- `--ipv4-addresses IPV4_ADDRESSES`
- `The total count of IPv4 addresses for this server. If`
- `specified this is the absolute value, not just the`
- `additional IPv4 addresses above what is included in`
- `the size. Leave null to accept the default for the`
- `size if this is a new server or to keep the current`
- `value if this is a resize of an existing server. Must`
- `not exceed the size.ipv4_addresses_max value.`
- `--memory MEMORY       The total memory in MB for this server.`
- `--disk DISK           The total storage in GB for this server.`
- `--transfer TRANSFER   The total transfer per month in TB for this server.`
- `--ipv4-addresses-to-remove [IPV4_ADDRESSES_TO_REMOVE ...]`
- `If you are reducing the number of IPv4 addresses you`
- `must specify which addresses to remove. If you specify`
- `more IPv4 addresses to remove than the number of IPv4`
- `addresses being removed the extra IPv4 addresses will`
- `be re-provisioned with new addresses.`

Change Image:
- `This may be left null to keep the current base image for the server. If`
- `this is provided the server disks will be destroyed and the server will be`
- `rebuilt from the selected image.`

- `--image IMAGE         The slug or ID of the selected image. What type of`
- `image is permitted here varies based on the server`
- `action.`
- `--name NAME           The hostname for the server. Leave null to accept the`
- `auto-generated permalink.`
- `--ssh-keys [SSH_KEYS ...]`
- `This may be either the existing SSH Keys IDs or`
- `fingerprints.`
- `--user-data USER_DATA`
- `If provided this will be used to initialise the new`
- `server. This must be left null if the Image does not`
- `support UserData, see DistributionInfo.Features for`
- `more information.`
- `--password PASSWORD   If this is provided the default remote user account's`
- `password will be set to this value. If this is null a`
- `random password will be generated and emailed to the`
- `account email address.`

Change Licenses:
- `This may be left null to keep the current licenses for the server. If this`
- `is provided any licenses that are not included will be removed.`

Licenses:
- `The desired set of licenses.`

- `+license              Required marker at start of each item.`
- `--software-id SOFTWARE_ID`
- `The ID of the software to license.`
- `--count COUNT         The number of licences.`

Pre Action Backup:
- `Specify this to create a backup before any actions are taken, or leave`
- `null to skip.`

- `--replacement-strategy REPLACEMENT_STRATEGY`
- `The strategy for selecting which backup to replace (if`
- `any). (One of: none, specified, oldest, newest)`
- `--backup-type BACKUP_TYPE`
- `If replacement_strategy is anything other than`
- `'specified', this must be provided. (One of: daily,`
- `weekly, monthly, temporary)`
- `--backup-id-to-replace BACKUP_ID_TO_REPLACE`
- `If replacement_strategy is 'specified' this property`
- `must be set to an existing backup.`
- `--label LABEL         An optional label to identify the backup.`


## bl server action resize-disk

usage: bl server action resize-disk [OPTIONS] SERVER --disk-id DISK_ID --size-gigabytes SIZE_GIGABYTES

Alter the size of an existing disk for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--disk-id DISK_ID     The ID of the existing disk. See server.disks for a`
- `list of IDs.`
- `--size-gigabytes SIZE_GIGABYTES`
- `The new size of the disk in GB. If increasing the size`
- `of the disk the server must have sufficient`
- `unallocated storage space.`


## bl server action restore

usage: bl server action restore [OPTIONS] SERVER --image IMAGE

Restore a backup to a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`
- `--image IMAGE      The ID of the specific backup to use. Snapshots are not`
- `currently supported.`


## bl server action shutdown

usage: bl server action shutdown [OPTIONS] SERVER

Request a server perform a shutdown

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action take-backup

usage: bl server action take-backup [OPTIONS] SERVER --replacement-strategy REPLACEMENT_STRATEGY [PARAMETERS]

Take a backup of a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server on which the action`
- `should be performed.`
- `--replacement-strategy REPLACEMENT_STRATEGY`
- `The strategy for selecting which backup to replace (if`
- `any). (One of: none, specified, oldest, newest)`

Parameters:
- `--backup-type BACKUP_TYPE`
- `If replacement_strategy is anything other than`
- `'specified', this must be provided. (One of: daily,`
- `weekly, monthly, temporary)`
- `--backup-id-to-replace BACKUP_ID_TO_REPLACE`
- `If replacement_strategy is 'specified' this property`
- `must be set to an existing backup.`
- `--label LABEL         An optional label to identify the backup.`


## bl server action uncancel

usage: bl server action uncancel [OPTIONS] SERVER

Revert the cancellation of a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server action uptime

usage: bl server action uptime [OPTIONS] SERVER

Check the uptime of a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`
- `--async            Do not wait for requested action to complete`
- `--quiet            Do not show progress while waiting for requested action`
- `to complete`

Arguments:
- `SERVER             The ID or name of the server on which the action should`
- `be performed.`


## bl server alert

usage: bl server alert [OPTIONS] COMMAND

Access server alert commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `get                Fetch the currently set threshold alerts for a server`
- `list               List any servers that have a current exceeded threshold`
- `alert`


## bl server alert get

Command '['bl', 'server', 'alert', 'get', '--help']' returned non-zero exit status 4294967295.

## bl server alert list

usage: bl server alert list [OPTIONS] 

List any servers that have a current exceeded threshold alert

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`


## bl server alert alert

Command '['bl', 'server', 'alert', 'alert', '--help']' returned non-zero exit status 2.

## bl server backup

usage: bl server backup [OPTIONS] COMMAND

Access server backup commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `list               List all backups for a server`
- `upload             Upload a backup for a server`


## bl server backup list

usage: bl server backup list [OPTIONS] SERVER

List all backups for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default:`
- `"id,slug,distribution,name")`
- `-1, --single-column   List one id per line.`

Arguments:
- `SERVER                The ID or name of the server for which backups should`
- `be listed.`

Available fields:
- `id                    The ID of this image.`
- `name                  If this is an operating system image, this is the name`
- `of the operating system version. If this is a backup`
- `image, this is the label of the backup if it exists,`
- `otherwise it is the UTC timestamp of the creation of`
- `the image.`
- `type                  One of the following values:`
- `custom - An image uploaded by a user.`
- `snapshot - A snapshot. Snapshot creation is not`
- `currently supported so only distribution images will`
- `have this value.`
- `backup - A backup of a server.`
- `public                A public image is available to all users. A private`
- `image is available only to the account that created`
- `the image.`
- `regions               The slugs of the regions where the image is available`
- `for use.`
- `min_disk_size         For a distribution image this is the minimum disk size`
- `in GB required to install the operating system. For a`
- `backup image this is the minimum total disk size in GB`
- `required to restore the backup.`
- `size_gigabytes        For a distribution image this is the disk size used in`
- `GB by the operating system on initial install. For a`
- `backup image this is the size of the compressed backup`
- `image in GB.`
- `status                One of the following values:`
- `NEW - The image is new.`
- `available - The image is available for use.`
- `pending - The image is pending and is not yet`
- `available for use.`
- `deleted - The image has been deleted and is no`
- `longer available for use.`
- `distribution_info     This object may provide further information about the`
- `distribution.`
- `distribution          If this is an operating system image, this is the name`
- `of the distribution. If this is a backup image, this`
- `is the name of the distribution the server is using.`
- `full_name             If this is an operating system image, this is the name`
- `and version of the distribution. If this is a backup`
- `image, this is the server hostname and label of the`
- `backup if it exists, otherwise it is the server`
- `hostname and UTC timestamp of the creation of the`
- `image.`
- `slug                  If this is an operating system image this is a slug`
- `which may be used as an alternative to the ID as a`
- `reference.`
- `created_at            If this is a backup image this is the date and time in`
- `ISO8601 format when the image was created.`
- `description           A description that may provide further details or`
- `warnings about the image.`
- `error_message         If the image creation failed this may provide further`
- `information.`
- `min_memory_megabytes  This is minimum memory in MB necessary to support this`
- `operating system (or the base operating system for a`
- `backup image).`
- `distribution_surcharges`
- `If this is not null the use of this image may incur`
- `surcharges above the base cost of the server. All`
- `costs are in AU$.`
- `backup_info           If this image is a backup, this object will provide`
- `further information.`


## bl server backup upload

usage: bl server backup upload [OPTIONS] SERVER --replacement-strategy REPLACEMENT_STRATEGY --url URL [PARAMETERS]

Upload a backup for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The ID or name of the server for which the backup is`
- `to be uploaded.`
- `--replacement-strategy REPLACEMENT_STRATEGY`
- `The strategy for selecting which backup to replace (if`
- `any). (One of: none, specified, oldest, newest)`
- `--url URL             The source URL for the image to upload. Only HTTP and`
- `HTTPS sources are currently supported.`

Parameters:
- `--backup-type BACKUP_TYPE`
- `If replacement_strategy is anything other than`
- `'specified', this must be provided. (One of: daily,`
- `weekly, monthly, temporary)`
- `--backup-id-to-replace BACKUP_ID_TO_REPLACE`
- `If replacement_strategy is 'specified' this property`
- `must be set to an existing backup.`
- `--label LABEL         An optional label to identify the backup.`


## bl server console

usage: bl server console [OPTIONS] SERVER

Fetch the console URLs for a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `SERVER             The ID or name of the server for which console URLs will`
- `be fetched.`


## bl server create

usage: bl server create [OPTIONS] --size SIZE --image IMAGE --region REGION [PARAMETERS] [+license ... ]

Create a new server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `--size SIZE           The slug of the selected size.`
- `--image IMAGE         The slug or id of the selected operating system.`
- `--region REGION       The slug of the selected region.`

Parameters:
- `--name NAME           The hostname of your server, such as`
- `vps01.yourcompany.com. If not provided, the server`
- `will be created with a random name.`
- `--backups, --no-backups`
- `If true this will enable two daily backups for the`
- `server. Options.daily_backups will override this value`
- `if provided. Setting this to false has no effect.`
- `--ipv6, --no-ipv6     If true this will enable IPv6 for this server.`
- `--vpc-id VPC_ID       Leave null to use default (public) network for the`
- `selected region.`
- `--ssh-keys [SSH_KEYS ...]`
- `This may be either the SSH keys Ids or fingerprints.`
- `If this is null or not provided any SSH keys that have`
- `been marked as default will be deployed (if the`
- `operating system supports SSH keys). Submit an empty`
- `array to disable deployment of default keys.`
- `--daily-backups DAILY_BACKUPS`
- `Leave null to accept the default for the size if this`
- `is a new server or to keep the current value if this`
- `is a resize of an existing server.`
- `--weekly-backups WEEKLY_BACKUPS`
- `Leave null to accept the default for the size if this`
- `is a new server or to keep the current value if this`
- `is a resize of an existing server.`
- `--monthly-backups MONTHLY_BACKUPS`
- `Leave null to accept the default for the size if this`
- `is a new server or to keep the current value if this`
- `is a resize of an existing server.`
- `--offsite-backups, --no-offsite-backups`
- `Leave null to accept the default for the size if this`
- `is a new server or to keep the current value if this`
- `is a resize of an existing server.`
- `--ipv4-addresses IPV4_ADDRESSES`
- `The total count of IPv4 addresses for this server. If`
- `specified this is the absolute value, not just the`
- `additional IPv4 addresses above what is included in`
- `the size. Leave null to accept the default for the`
- `size if this is a new server or to keep the current`
- `value if this is a resize of an existing server. Must`
- `not exceed the size.ipv4_addresses_max value.`
- `--memory MEMORY       The total memory in MB for this server.`
- `--disk DISK           The total storage in GB for this server.`
- `--transfer TRANSFER   The total transfer per month in TB for this server.`
- `--user-data USER_DATA`
- `If provided this will be used to initialise the new`
- `server. This must be left null if the Image does not`
- `support UserData, see DistributionInfo.Features for`
- `more information.`
- `--port-blocking, --no-port-blocking`
- `Port blocking of outgoing connections for email, SSH`
- `and Remote Desktop (TCP ports 22, 25, and 3389) is`
- `enabled by default for all new servers. If this is`
- `false port blocking will be disabled. Disabling port`
- `blocking is only available to reviewed accounts.`
- `--password PASSWORD   If this is provided the default remote user account's`
- `password will be set to this value. If this is null a`
- `random password will be generated and emailed to the`
- `account email address.`

Licenses:
- `The desired set of licenses.`

- `+license              Required marker at start of each item.`
- `--software-id SOFTWARE_ID`
- `The ID of the software to license.`
- `--count COUNT         The number of licences.`


## bl server data-usage

usage: bl server data-usage [OPTIONS] COMMAND

Access server data-usage commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `get                Fetch the current data usage (Transfer) for a server`
- `list               Fetch all current data usage (Transfer) for all servers`


## bl server data-usage get

usage: bl server data-usage get [OPTIONS] SERVER

Fetch the current data usage (Transfer) for a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `SERVER             The target server id or name.`


## bl server data-usage list

usage: bl server data-usage list [OPTIONS] 

Fetch all current data usage (Transfer) for all servers

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "server_id,expires,trans`
- `fer_gigabytes,current_transfer_usage_gigabytes,transfe`
- `r_period_end")`
- `-1, --single-column   List one server_id per line.`

Available fields:
- `server_id             The ID of the server that this data transfer usage`
- `refers to.`
- `expires               The date and time in ISO8601 format that the current`
- `billing period expires.`
- `transfer_gigabytes    The included data transfer for this server in this`
- `period in GB.`
- `current_transfer_usage_gigabytes`
- `The used data transfer for this server in this period`
- `in GB.`
- `If you have more than one server, please see our data`
- `pooling policy: this value may include excess data`
- `transfer used by other servers or may have 'offloaded'`
- `excess data transfer to other servers with spare`
- `capacity.`
- `transfer_period_end   The date and time in ISO8601 format that the data`
- `transfer limit period ended (if it is completed) or`
- `when it will end (if this is the current period).`


## bl server delete

usage: bl server delete [OPTIONS] SERVER [PARAMETERS]

Cancel an existing server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `SERVER             The ID or name of the server to be cancelled.`

Parameters:
- `--reason REASON    The reason for cancelling the server.`


## bl server failover-ip

usage: bl server failover-ip [OPTIONS] COMMAND

Access server failover-ip commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `available          Fetch a list of all failover IPs that are available to be`
- `assigned to a server`
- `get                Fetch the failover IPs for a server`
- `update             Sets the list of failover IPs that are assigned to a`
- `server`


## bl server failover-ip available

usage: bl server failover-ip available [OPTIONS] SERVER

Fetch a list of all failover IPs that are available to be assigned to a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `SERVER             The target server id or name.`


## bl server failover-ip assigned

Command '['bl', 'server', 'failover-ip', 'assigned', '--help']' returned non-zero exit status 2.

## bl server failover-ip get

usage: bl server failover-ip get [OPTIONS] SERVER

Fetch the failover IPs for a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `SERVER             The target server id or name.`


## bl server failover-ip update

usage: bl server failover-ip update [OPTIONS] SERVER --failover-ips FAILOVER_IPS

Sets the list of failover IPs that are assigned to a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `SERVER                The target server id or name.`
- `--failover-ips [FAILOVER_IPS ...]`
- `The list of failover IP addresses to assign to this`
- `server. This overwrites the current list, so any`
- `current failover IP addresses that are omitted will be`
- `removed from the server.`


## bl server failover-ip server

Command '['bl', 'server', 'failover-ip', 'server', '--help']' returned non-zero exit status 2.

## bl server feature

usage: bl server feature [OPTIONS] COMMAND

Access server feature commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `list               Fetch the currently available advanced features for a`
- `server`


## bl server feature list

usage: bl server feature list [OPTIONS] SERVER

Fetch the currently available advanced features for a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `SERVER             The ID or name of the server for which advanced features`
- `should be listed.`


## bl server feature server

Command '['bl', 'server', 'feature', 'server', '--help']' returned non-zero exit status 2.

## bl server firewall

usage: bl server firewall [OPTIONS] COMMAND

Access server firewall commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `list               Fetch all advanced firewall rules for a server`


## bl server firewall list

usage: bl server firewall list [OPTIONS] SERVER

Fetch all advanced firewall rules for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "source_addresses,destin`
- `ation_addresses,protocol,destination_ports,action,desc`
- `ription")`
- `-1, --single-column   List one source_addresses per line.`

Arguments:
- `SERVER                The ID or name of the server for which firewall rules`
- `should be listed.`

Available fields:
- `source_addresses      The source addresses to match for this rule. Each`
- `address may be an individual IPv4 address or a range`
- `in IPv4 CIDR notation.`
- `destination_addresses`
- `The destination addresses to match for this rule. Each`
- `address may be an individual IPv4 address or a range`
- `in IPv4 CIDR notation.`
- `protocol              The protocol to match for this rule.`
- `action                The action to take when there is a match on this rule.`
- `destination_ports     The destination ports to match for this rule. Leave`
- `null or empty to match on all ports.`
- `description           A description to assist in identifying this rule.`
- `Commonly used to record the reason for the rule or the`
- `intent behind it, e.g. "Block access to RDP" or "Allow`
- `access from HQ".`


## bl server get

usage: bl server get [OPTIONS] SERVER

Fetch an existing server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `SERVER             The ID or name of the server to fetch.`


## bl server ipv6-ptr-ns

usage: bl server ipv6-ptr-ns [OPTIONS] COMMAND

Access server ipv6-ptr-ns commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `list               Fetch all existing IPv6 name server records`
- `update             Create new or update existing IPv6 name server records`


## bl server ipv6-ptr-ns list

usage: bl server ipv6-ptr-ns list [OPTIONS] 

Fetch all existing IPv6 name server records

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`


## bl server ipv6-ptr-ns update

usage: bl server ipv6-ptr-ns update [OPTIONS] --reverse-nameservers REVERSE_NAMESERVERS

Create new or update existing IPv6 name server records

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--async               Do not wait for requested action to complete`
- `--quiet               Do not show progress while waiting for requested`
- `action to complete`

Arguments:
- `--reverse-nameservers [REVERSE_NAMESERVERS ...]`
- `A list of all IPv6 reverse name servers for this`
- `server. Any existing reverse name servers that are`
- `omitted from the list will be removed from the server.`


## bl server kernel

usage: bl server kernel [OPTIONS] COMMAND

Access server kernel commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `list               List all available kernels for a server`


## bl server kernel list

usage: bl server kernel list [OPTIONS] SERVER

List all available kernels for a server

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...   Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "id,name,version")`
- `-1, --single-column  List one id per line.`

Arguments:
- `SERVER               The ID or name of the server for which kernels should`
- `be listed.`

Available fields:
- `id                   The ID of this kernel.`
- `name                 This name of this kernel.`
- `version              The version (if any) of this kernel.`


## bl server list

usage: bl server list [OPTIONS] [PARAMETERS]

List all servers

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default:`
- `"id,name,image,vcpus,memory,disk,region,networks")`
- `-1, --single-column   List one id per line.`

Parameters:
- `--hostname HOSTNAME   Providing a hostname restricts the results to the`
- `server that has this hostname (case insensitive). If`
- `this parameter is provided at most 1 server will be`
- `returned.`

Available fields:
- `id                    The ID of this server.`
- `name                  The hostname of this server.`
- `memory                The memory in MB of this server.`
- `vcpus                 The number of virtual CPUs of this server.`
- `disk                  The total disk in GB of this server.`
- `created_at            The date and time in ISO8601 format of this server's`
- `initial creation.`
- `status                One of the following values:`
- `new - The server is currently in the process of`
- `building and is not yet available for use.`
- `active - The server is available for use.`
- `archive - The server is powered off due to`
- `cancellation or non payment.`
- `off - The server has been powered off, but may be`
- `powered back on.`
- `backup_ids            A list of the currently existing backup image IDs for`
- `this server (if any).`
- `features              A list of the currently enabled features on this`
- `server.`
- `region                The region this server is allocated to.`
- `image                 The base image used to create this server.`
- `size                  The currently selected size for this server.`
- `size_slug             The slug of the currently selected size for this`
- `server.`
- `networks              A list of the networks of the server.`
- `disks                 A list of the disks that are currently attached to the`
- `server.`
- `backup_settings       Detailed backup settings for the server.`
- `failover_ips          A list of any assigned failover IP addresses for this`
- `server.`
- `host                  Summary information about the host of this server.`
- `password_change_supported`
- `If this is true the password_reset server action can`
- `be called to change a user's password. If this is`
- `false the password_reset server action will merely`
- `clear the root/administrator password allowing the`
- `password to be changed via the web console.`
- `advanced_features     The currently enabled advanced features, machine type`
- `and processor flags.`
- `vpc_id                The VPC ID that this server is allocated to. If this`
- `value is null the server is in the default (public)`
- `network for the region.`
- `selected_size_options`
- `An object that details the selected options for the`
- `current size.`
- `kernel                The currently selected kernel for the server.`
- `next_backup_window    The details of the next scheduled backup, if any.`
- `cancelled_at          If the server has been cancelled, this is the date and`
- `time in ISO8601 format of that cancellation.`
- `partner_id            The server ID of the partner of this server, if one`
- `has been assigned.`
- `permalink             A randomly generated two-word identifier assigned to`
- `servers in regions that support this feature.`
- `attached_backup       An object that provides details of any backup image`
- `currently attached to the server..`


## bl server metrics

usage: bl server metrics [OPTIONS] COMMAND

Access server metrics commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `get                Fetch the latest performance and usage data sample set`
- `for a server`
- `list               Fetch all of the performance and usage data sample sets`
- `for a server`


## bl server metrics get

usage: bl server metrics get [OPTIONS] SERVER [PARAMETERS]

Fetch the latest performance and usage data sample set for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `SERVER                The target server id or name.`

Parameters:
- `--data-interval DATA_INTERVAL`
- `| Value | Description |`
- `| ----- | ----------- |`
- `| five-minute | 5 Minutes |`
- `| half-hour | 30 Minutes |`
- `| four-hour | 4 Hours |`
- `| day | 1 Day |`
- `| week | 7 Days |`
- `| month | 1 Month |`
- `(One of: five-minute, half-hour, four-hour, day,`
- `week, month)`


## bl server metrics for

Command '['bl', 'server', 'metrics', 'for', '--help']' returned non-zero exit status 2.

## bl server metrics list

usage: bl server metrics list [OPTIONS] SERVER [PARAMETERS]

Fetch all of the performance and usage data sample sets for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "server_id,maximum_memor`
- `y_megabytes,maximum_storage_gigabytes")`
- `-1, --single-column   List one server_id per line.`

Arguments:
- `SERVER                The target server id or name.`

Parameters:
- `--data-interval DATA_INTERVAL`
- `| Value | Description |`
- `| ----- | ----------- |`
- `| five-minute | 5 Minutes |`
- `| half-hour | 30 Minutes |`
- `| four-hour | 4 Hours |`
- `| day | 1 Day |`
- `| week | 7 Days |`
- `| month | 1 Month |`
- `(One of: five-minute, half-hour, four-hour, day,`
- `week, month)`
- `--start START         The start of the window of samples to retrieve,`
- `ISO8601 format (eg 2022-12-30T22:50:00Z). Defaults to`
- `1 week before end for intervals larger than 5 minutes,`
- `or 1 day for 5 minute intervals.`
- `--end END             The start of the window of samples to retrieve,`
- `ISO8601 format (eg 2022-12-30T22:50:00Z). Defaults to`
- `1 week or 1 day after start date depending on the`
- `selected data interval (or the current time if start`
- `is not provided). Can't be more than 1 year from`
- `start.`

Available fields:
- `server_id             The ID of the server that this sample set refers to.`
- `period                The period when this sample set was collected.`
- `average               The average values of the samples collected during`
- `this period.`
- `maximum_memory_megabytes`
- `The maximum memory used in MB at any point during this`
- `collection period.`
- `maximum_storage_gigabytes`
- `The maximum storage used in GB at any point during`
- `this collection period.`


## bl server metrics for

Command '['bl', 'server', 'metrics', 'for', '--help']' returned non-zero exit status 2.

## bl server snapshot

usage: bl server snapshot [OPTIONS] COMMAND

Access server snapshot commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `list               List all snapshots for a server`


## bl server snapshot list

usage: bl server snapshot list [OPTIONS] SERVER

List all snapshots for a server

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default:`
- `"id,slug,distribution,name")`
- `-1, --single-column   List one id per line.`

Arguments:
- `SERVER                The ID or name of the server for which snapshots`
- `should be listed.`

Available fields:
- `id                    The ID of this image.`
- `name                  If this is an operating system image, this is the name`
- `of the operating system version. If this is a backup`
- `image, this is the label of the backup if it exists,`
- `otherwise it is the UTC timestamp of the creation of`
- `the image.`
- `type                  One of the following values:`
- `custom - An image uploaded by a user.`
- `snapshot - A snapshot. Snapshot creation is not`
- `currently supported so only distribution images will`
- `have this value.`
- `backup - A backup of a server.`
- `public                A public image is available to all users. A private`
- `image is available only to the account that created`
- `the image.`
- `regions               The slugs of the regions where the image is available`
- `for use.`
- `min_disk_size         For a distribution image this is the minimum disk size`
- `in GB required to install the operating system. For a`
- `backup image this is the minimum total disk size in GB`
- `required to restore the backup.`
- `size_gigabytes        For a distribution image this is the disk size used in`
- `GB by the operating system on initial install. For a`
- `backup image this is the size of the compressed backup`
- `image in GB.`
- `status                One of the following values:`
- `NEW - The image is new.`
- `available - The image is available for use.`
- `pending - The image is pending and is not yet`
- `available for use.`
- `deleted - The image has been deleted and is no`
- `longer available for use.`
- `distribution_info     This object may provide further information about the`
- `distribution.`
- `distribution          If this is an operating system image, this is the name`
- `of the distribution. If this is a backup image, this`
- `is the name of the distribution the server is using.`
- `full_name             If this is an operating system image, this is the name`
- `and version of the distribution. If this is a backup`
- `image, this is the server hostname and label of the`
- `backup if it exists, otherwise it is the server`
- `hostname and UTC timestamp of the creation of the`
- `image.`
- `slug                  If this is an operating system image this is a slug`
- `which may be used as an alternative to the ID as a`
- `reference.`
- `created_at            If this is a backup image this is the date and time in`
- `ISO8601 format when the image was created.`
- `description           A description that may provide further details or`
- `warnings about the image.`
- `error_message         If the image creation failed this may provide further`
- `information.`
- `min_memory_megabytes  This is minimum memory in MB necessary to support this`
- `operating system (or the base operating system for a`
- `backup image).`
- `distribution_surcharges`
- `If this is not null the use of this image may incur`
- `surcharges above the base cost of the server. All`
- `costs are in AU$.`
- `backup_info           If this image is a backup, this object will provide`
- `further information.`


## bl server software

usage: bl server software [OPTIONS] SERVER

List all enabled software for a server

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...   Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "licence_count")`
- `-1, --single-column  List one licence_count per line.`

Arguments:
- `SERVER               The ID or name of the server for which software should`
- `be fetched.`

Available fields:
- `software             The currently licensed software.`
- `licence_count        The current licence count for the software.`


## bl server user-data

usage: bl server user-data [OPTIONS] SERVER

Fetch the currently set UserData for a server

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `SERVER             The ID or name of the server for which userdata should be`
- `fetched.`


## bl size

usage: bl size [OPTIONS] COMMAND

Access size commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `list               List all available sizes`


## bl size list

usage: bl size list [OPTIONS] [PARAMETERS]

List all available sizes

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "slug,size_type,vcpus,vc`
- `pu_units,memory,disk,transfer,price_monthly")`
- `-1, --single-column   List one slug per line.`

Parameters:
- `--server-id SERVER_ID`
- `If supplied only sizes available for a resize the`
- `specified server will be returned. This parameter is`
- `only available when authenticated.`
- `--image IMAGE         If null or not provided regions that support the size`
- `are included in the returned objects regardless of`
- `operating system. If this is provided it must be the`
- `id or slug of an operating system image and will cause`
- `only valid regions for the size and operating system`
- `to be included in the returned objects.`

Available fields:
- `slug                  The slug of this size.`
- `size_type             The type of this size, generally used to differentiate`
- `sizes optimized for different usages.`
- `available             If this is false the size is not available for new`
- `servers.`
- `regions               A list of region slugs where this size is available`
- `regardless of stock.`
- `If this a response to a query that included a selected`
- `operating system this response will only include`
- `regions where that operating system is available on`
- `this size,`
- `otherwise not all regions listed will support all`
- `operating systems on this size.`
- `price_monthly         Monthly Price in AU$.`
- `price_hourly          Hourly price in AU$.`
- `disk                  The included storage for this size in GB.`
- `memory                The included memory for this size in MB.`
- `transfer              The included data transfer for this size in TB.`
- `excess_transfer_cost_per_gigabyte`
- `The excess charged for any transfer above the included`
- `data transfer in AU$ per GB.`
- `vcpus                 The count of virtual CPUs for this size. See`
- `vcpu_units for a description of how each virtual CPU`
- `maps to the underlying hardware.`
- `vcpu_units            This is the unit that the vcpus field counts, e.g.`
- `"core" or "thread".`
- `options               Available add-ons (optional features not included in`
- `the base price) for the size. All costs are in AU$ per`
- `month (pro-rated).`
- `description           A description of this size.`
- `cpu_description       A description of the CPU provided in this size.`
- `storage_description   A description of the storage provided in this size.`
- `regions_out_of_stock  A list of region slugs where the size is normally`
- `available but is currently not available due to lack`
- `of stock.`


## bl software

usage: bl software [OPTIONS] COMMAND

Access software commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `get                Fetch existing software`
- `list               List all available software`
- `operating-system   List all available software for an existing operating`
- `system`


## bl software get

usage: bl software get [OPTIONS] SOFTWARE_ID

Fetch existing software

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `SOFTWARE_ID        The ID of the software to fetch.`


## bl software list

usage: bl software list [OPTIONS] 

List all available software

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default:`
- `"id,name,description,cost_per_licence_per_month")`
- `-1, --single-column   List one id per line.`

Available fields:
- `id                    The ID of this software.`
- `enabled               Software that is not enabled is not available to be`
- `added to servers but may be retained by servers that`
- `currently use it.`
- `name                  The name of this software.`
- `description           The description of this software.`
- `cost_per_licence_per_month`
- `The cost for each licence of this software per month`
- `in AU$.`
- `minimum_licence_count`
- `The minimum licences permitted for this software.`
- `maximum_licence_count`
- `The maximum licences permitted for this software.`
- `licence_step_count    Licences must be purchased in multiples of this value.`
- `supported_operating_systems`
- `A list of slugs of operating system images that`
- `support this software.`
- `group                 Software in the same group may not be licensed`
- `together.`


## bl software operating-system

usage: bl software operating-system [OPTIONS] OPERATING_SYSTEM_ID_OR_SLUG

List all available software for an existing operating system

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default:`
- `"id,name,description,cost_per_licence_per_month")`
- `-1, --single-column   List one id per line.`

Arguments:
- `OPERATING_SYSTEM_ID_OR_SLUG`
- `The ID or slug of the operating system for which`
- `available software should be listed.`

Available fields:
- `id                    The ID of this software.`
- `enabled               Software that is not enabled is not available to be`
- `added to servers but may be retained by servers that`
- `currently use it.`
- `name                  The name of this software.`
- `description           The description of this software.`
- `cost_per_licence_per_month`
- `The cost for each licence of this software per month`
- `in AU$.`
- `minimum_licence_count`
- `The minimum licences permitted for this software.`
- `maximum_licence_count`
- `The maximum licences permitted for this software.`
- `licence_step_count    Licences must be purchased in multiples of this value.`
- `supported_operating_systems`
- `A list of slugs of operating system images that`
- `support this software.`
- `group                 Software in the same group may not be licensed`
- `together.`


## bl software system

Command '['bl', 'software', 'system', '--help']' returned non-zero exit status 2.

## bl ssh-key

usage: bl ssh-key [OPTIONS] COMMAND

Access ssh-key commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `create             Add a new SSH key`
- `delete             Delete an existing SSH key`
- `get                Fetch an existing SSH key`
- `list               List all SSH keys`
- `update             Update an existing SSH key`


## bl ssh-key create

usage: bl ssh-key create [OPTIONS] --public-key PUBLIC_KEY --name NAME [PARAMETERS]

Add a new SSH key

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `--public-key PUBLIC_KEY`
- `The public key in OpenSSH "authorized_keys" format.`
- `--name NAME           A name to help you identify the key.`

Parameters:
- `--default, --no-default`
- `Optional: If true this will be added to all new server`
- `installations (if we support SSH Key injection for the`
- `server's operating system).`


## bl ssh-key delete

usage: bl ssh-key delete [OPTIONS] KEY_ID

Delete an existing SSH key

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `KEY_ID             The ID or fingerprint of the SSH Key to delete.`


## bl ssh-key get

usage: bl ssh-key get [OPTIONS] KEY_ID

Fetch an existing SSH key

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `KEY_ID             The ID or fingerprint of the SSH Key to fetch.`


## bl ssh-key list

usage: bl ssh-key list [OPTIONS] 

List all SSH keys

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...   Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default:`
- `"id,name,default,fingerprint")`
- `-1, --single-column  List one id per line.`

Available fields:
- `id                   The ID of this SSH key.`
- `fingerprint          The fingerprint of this SSH key.`
- `public_key           The public key of this SSH key.`
- `default              If an SSH key is marked as default it will be deployed`
- `to all newly created servers that support SSH keys`
- `unless expressly overridden in the creation request.`
- `name                 The name of this SSH key. This is used only to aid in`
- `identification.`


## bl ssh-key update

usage: bl ssh-key update [OPTIONS] KEY_ID --name NAME [PARAMETERS]

Update an existing SSH key

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `KEY_ID                The ID or fingerprint of the SSH Key to update.`
- `--name NAME           A name to help you identify the key.`

Parameters:
- `--default, --no-default`
- `Do not provide or leave null to leave the default`
- `status of the key unchanged.`


## bl version

bl version 0.16.0


## bl vpc

usage: bl vpc [OPTIONS] COMMAND

Access vpc commands

Options:
- `--help             Display available commands and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`

Available Commands:
- `create             Create a new VPC`
- `delete             Delete an existing VPC`
- `get                Fetch an existing VPC`
- `list               List all existing VPCs`
- `members            List all members of an existing VPC`
- `patch              Update an existing VPC`
- `update             Update an existing VPC`


## bl vpc create

usage: bl vpc create [OPTIONS] --name NAME [PARAMETERS] [+route ... ]

Create a new VPC

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `--name NAME           A name to help identify this VPC.`

Parameters:
- `--ip-range IP_RANGE   A private address range that you select during`
- `creation, such as the default value of 10.240.0.0/16.`
- `Because the virtual network is dedicated to your use,`
- `you may use whatever IP address range you like.`

Route Entries:
- `The route entries that control how network traffic is directed through the`
- `VPC environment.`

- `+route                Required marker at start of each item.`
- `--router ROUTER       The server that will receive traffic sent to the`
- `destination property in this VPC.`
- `--destination DESTINATION`
- `The destination address for this route entry. This may`
- `be in CIDR format.`
- `--description DESCRIPTION`
- `An optional description for the route.`


## bl vpc delete

usage: bl vpc delete [OPTIONS] VPC_ID

Delete an existing VPC

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `VPC_ID             The target vpc id.`


## bl vpc get

usage: bl vpc get [OPTIONS] VPC_ID

Fetch an existing VPC

Options:
- `--help             Display command options and descriptions`
- `--context NAME     Name of authentication context to use (default: "bl")`
- `--api-token VALUE  API token to use with BinaryLane API`
- `--curl             Display API request as a 'curl' command-line`
- `--no-header        Display columns without field labels`
- `--output OUTPUT    Desired output format [plain, table, tsv, json] (default:`
- `"table")`

Arguments:
- `VPC_ID             The target vpc id.`


## bl vpc list

usage: bl vpc list [OPTIONS] 

List all existing VPCs

Options:
- `--help               Display command options and descriptions`
- `--context NAME       Name of authentication context to use (default: "bl")`
- `--api-token VALUE    API token to use with BinaryLane API`
- `--curl               Display API request as a 'curl' command-line`
- `--no-header          Display columns without field labels`
- `--output OUTPUT      Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...   Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default: "id,name,ip_range")`
- `-1, --single-column  List one id per line.`

Available fields:
- `id                   The ID of this VPC.`
- `name                 The name of this VPC.`
- `ip_range             The IPv4 range for this VPC in CIDR format.`
- `route_entries        The route entries that control how network traffic is`
- `directed through the VPC environment.`


## bl vpc members

usage: bl vpc members [OPTIONS] VPC_ID [PARAMETERS]

List all members of an existing VPC

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`
- `--format FIELD,...    Comma-separated list of fields to display. Wildcards`
- `are supported:                 e.g. --format "*" will`
- `display all fields. (default:`
- `"name,resource_type,resource_id")`
- `-1, --single-column   List one name per line.`

Arguments:
- `VPC_ID                The target vpc id.`

Parameters:
- `--resource-type RESOURCE_TYPE`
- `| Value | Description |`
- `| ----- | ----------- |`
- `| server | Server |`
- `| load-balancer | Load Balancer |`
- `| ssh-key | SSH Key |`
- `| vpc | Virtual Private Network |`
- `| image | Backup or Operating System Image |`
- `| registered-domain-name | Registered Domain Name |`
- `(One of: server, load-balancer, ssh-key, vpc, image,`
- `registered-domain-name)`

Available fields:
- `name                  The name of this VPC member.`
- `resource_type         One of the following values:`
- `server - Server`
- `load-balancer - Load Balancer`
- `ssh-key - SSH Key`
- `vpc - Virtual Private Network`
- `image - Backup or Operating System Image`
- `registered-domain-name - Registered Domain Name`
- `resource_id           The resource ID of this VPC member.`
- `created_at            The date and time in ISO8601 format of this resource's`
- `initial creation.`


## bl vpc patch

usage: bl vpc patch [OPTIONS] VPC_ID [PARAMETERS] [+route ... ]

Update an existing VPC

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `VPC_ID                The target vpc id.`

Parameters:
- `--name NAME           >A name to help identify this VPC. Submit null to`
- `leave unaltered.`

Route Entries:
- `Submit null to leave unaltered, submit an empty list to clear all route`
- `entries. It is not possible to PATCH individual route entries, to alter a`
- `route entry submit the entire list of route entries you wish to save.`

- `+route                Required marker at start of each item.`
- `--router ROUTER       The server that will receive traffic sent to the`
- `destination property in this VPC.`
- `--destination DESTINATION`
- `The destination address for this route entry. This may`
- `be in CIDR format.`
- `--description DESCRIPTION`
- `An optional description for the route.`


## bl vpc update

usage: bl vpc update [OPTIONS] VPC_ID --name NAME [+route ... ]

Update an existing VPC

Options:
- `--help                Display command options and descriptions`
- `--context NAME        Name of authentication context to use (default: "bl")`
- `--api-token VALUE     API token to use with BinaryLane API`
- `--curl                Display API request as a 'curl' command-line`
- `--no-header           Display columns without field labels`
- `--output OUTPUT       Desired output format [plain, table, tsv, json]`
- `(default: "table")`

Arguments:
- `VPC_ID                The target vpc id.`
- `--name NAME           A name to help identify this VPC.`

Route Entries:
- `The route entries that control how network traffic is directed through the`
- `VPC environment.`

- `+route                Required marker at start of each item.`
- `--router ROUTER       The server that will receive traffic sent to the`
- `destination property in this VPC.`
- `--destination DESTINATION`
- `The destination address for this route entry. This may`
- `be in CIDR format.`
- `--description DESCRIPTION`
- `An optional description for the route.`


