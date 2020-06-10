# Roles and Permissions Support

SeaTable comes with two build-in roles `default` and `guest`.

> Note: roles and permissions are only supported in pro edition

## Edit build-in roles

If you want to edit the permissions of build-in roles,you can add following lines to `dtable_web_settings.py` with corresponding permissions set to `True`.

```
ENABLED_ROLE_PERMISSIONS = {
    'default': {
        'can_add_dtable': True,
        'can_add_group': True,
        'can_create_common_dataset': True,
        'can_generate_external_link': True
    },
    'guest': {
        'can_add_dtable': False,
        'can_add_group': False,
        'can_create_common_dataset': False,
    },
}

```

## Add custom roles

If you want to add a new role and assign some users with this role, e.g. new role `employee`. You can add following lines to `dtable_web_settings.py`.

```
ENABLED_ROLE_PERMISSIONS = {
    'default': {
        'can_add_dtable': True,
        'can_add_group': True,
        'can_create_common_dataset': True,
    },
    'guest': {
        'can_add_dtable': False,
        'can_add_group': False,
        'can_create_common_dataset': False,
    },
    'employee': {
        'can_add_dtable': True,
        'can_add_group': False,
        'can_create_common_dataset': False
    },
}

```


