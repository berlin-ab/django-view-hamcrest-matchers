# Django View Hamcrest Matchers

A collection of matchers for pyhamcrest to help while testing Django Views.


## Disclaimer

None of these matchers are implemented yet, but I'd really like them to be. 


    from django_view_hamcrest_matchers import *

    from django.test import Client

    class TestDjangoViewHamcrestMatchers(testunit.TestCase):
        def test_django_view_hamcrest_matchers(self):
            client = Client()
            response = client.do_something()
            assert_that(response, is_ok())
            assert_that(response, is_created())
            assert_that(response, is_not_authorized())
            assert_that(response, has_tag("h1", with_text="Voxy.com"))
            assert_that(response, has_json_entries({
              "user": {
                "id": 123,
              }
            }))


