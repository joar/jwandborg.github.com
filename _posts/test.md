---
layout: default
title: Test &ndash; Joar Wandborg
---
# Lorem ipsum

Dolor sit amet consecteteuer adipisicing elit.
    """
    Email verification view
    
    validates GET parameters against database and unlocks the user account, if
    you are lucky :)
    """
    import bson.objectid
    user = request.db.User.find_one(
    	{'_id': bson.objectid.ObjectId(unicode(request.GET.get('userid')))})
	
    verification_successful = bool

    if user and user['verification_key'] == unicode(request.GET.get('token')):
        user['status'] = u'active'
        user['email_verified'] = True
	verification_successful = True
	user.save()
    else:
        verification_successful = False
	
    template = request.template_env.get_template(
        'mediagoblin/auth/verify_email.html')
    return Response(
        template.render(
            {'request': request,
            'user': user,
	    'verification_successful': verification_successful}))
																		      
