# 9. Cost optimization

## Cost categories observed

- EC2 instance-hours;
- EBS GP3 provisioned storage;
- public IPv4 address-hours;
- optional log storage and monitoring.

## Actions taken

- Resized the instance from a larger type to a smaller instance appropriate for a static landing page.
- Stopped the instance when it was not needed during experimentation.
- Reviewed EBS and IPv4 charges separately from compute.
- Created a zero-spend budget notification.

## Important distinction

Stopping an EC2 instance stops instance compute charges, but attached EBS volumes remain provisioned and billable. Public IPv4 pricing depends on allocation and use; unused addresses should be released when they are no longer required.

## Lower-cost production alternatives

A static landing page can often be hosted more economically using object storage and a CDN rather than a continuously running virtual server. EC2 remains valuable here because the project was also a Linux, networking, and cloud-administration exercise.
