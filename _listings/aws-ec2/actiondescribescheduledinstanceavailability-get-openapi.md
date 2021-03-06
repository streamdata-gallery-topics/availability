---
swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 0
info:
  title: AWS EC2 API Describe Scheduled Instance Availability
  version: 1.0.0
  description: Finds available schedules that meet the specified criteria.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateVolume:
    get:
      summary: Create Volume
      description: Creates an EBS volume that can be attached to an instance in the
        same Availability Zone.
      operationId: createvolume
      x-api-path-slug: actioncreatevolume-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: SnapshotId
        description: The ID of the EBS snapshot
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volume
  /?Action=DescribeAvailabilityZones:
    get:
      summary: Describe Availability Zones
      description: Describes one or more of the Availability Zones that are available
        to you.
      operationId: describeavailabilityzones
      x-api-path-slug: actiondescribeavailabilityzones-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: RegionName.N
        description: The names of one or more regions
        type: string
      responses:
        200:
          description: OK
      tags:
      - Availability Zones
  /?Action=DescribeScheduledInstanceAvailability:
    get:
      summary: Describe Scheduled Instance Availability
      description: Finds available schedules that meet the specified criteria.
      operationId: describescheduledinstanceavailability
      x-api-path-slug: actiondescribescheduledinstanceavailability-get
      responses:
        200:
          description: OK
      tags:
      - Server Instance Availability
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---