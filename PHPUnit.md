A typical JWTAUth TestCase

```
<?php

namespace Tests;

use App\Models\User;
use Illuminate\Foundation\Testing\RefreshDatabase;
use Illuminate\Foundation\Testing\TestCase as BaseTestCase;
use Tymon\JWTAuth\Facades\JWTAuth;

abstract class ApiTestCase extends BaseTestCase
{
    use CreatesApplication, RefreshDatabase;

    protected bool $seed = true;

    protected function buildAuthenticationHttpRequest($userId): ApiTestCase
    {
        $user = User::find($userId);
        $token = JWTAuth::fromUser($user);

        return $this->withHeaders([
            'Authorization' => 'Bearer ' . $token,
            'Accept' => 'application/json'
        ]);
    }

    protected function getProfile($userId)
    {
        $request = $this->buildAuthenticationHttpRequest($userId);
        $response = $request->getJson('api/auth/me');
        return $response->json('data');
    }

}

```
